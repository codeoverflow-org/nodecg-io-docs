<style>
    a.contributorlink:hover {
        text-decoration-style: solid;
        text-decoration-line: underline;
        text-decoration-color: white;
    }
</style>

<script type="text/javascript">
    const REPOS = [
        'codeoverflow-org/nodecg-io',
        'codeoverflow-org/nodecg-io-docs',
        'codeoverflow-org/nodecg-io-cli'
    ];
    const BLACKLIST = [
        'dependabot[bot]',
        'semantic-release-bot'
    ];
    (async () => {
        // name -> { avatar?,  html_url, contributions }
        const contributors = {}
        for (const repo of REPOS) {
            const response = await fetch(`https://api.github.com/repos/${repo}/contributors`);
            const data = await response.json();
            data.forEach(entry => {
                if (!BLACKLIST.includes(entry.login)) {
                    if (!(entry.login in contributors)) {
                        contributors[entry.login] = {
                            avatar_url: entry.avatar_url,
                            html_url: entry.html_url,
                            contributions: 0
                        }
                    }
                    contributors[entry.login].contributions += entry.contributions
                }
            })
        }
        const sorted = Object.keys(contributors).sort((n1, n2) => {
            const result = contributors[n2].contributions - contributors[n1].contributions;
            // If the contributions are equal we sort by name
            return result == 0 ? n1.toLowerCase() < n2.toLowerCase() : result
        });
        let idx = 1
        console.log(contributors)
        console.log(Object.keys(contributors))
        for (const name of sorted) {
            const div = document.createElement('div')
            div.style = `grid-column: 1; grid-row: ${idx}; display: inline-block; padding-bottom: 10px`
            if ('avatar_url' in contributors[name]) {
                div.innerHTML = `
                  <img src="${contributors[name].avatar_url}" width="64" height="64" style="float: left; margin-top: 0">
                  <div style="float:left; margin-top: 0">
                    <span style="font-size: 16pt; font-weight: bold; margin-left: 1em; color: white;">
                      <a style="color: white;" class="contributorlink" href="${contributors[name].html_url}">${name}</a>
                    </span><br>
                    <span style="font-size: 12pt; margin-left: 1em; color: white;">
                      <a style="color: white;" class="contributorlink" href="https://github.com/codeoverflow-org/nodecg-io/commits?author=${name}">${contributors[name].contributions} contributions</a>
                    </span>
                  </div>
                `
            } else {
                div.innerHTML = `
                  <span style="font-size: 16pt; font-weight: bold; margin-left: 1em; color: white;">${name}</span><br>
                  <span style="font-size: 12pt; margin-left: 1em; color: white;">${contributors[name].contributions} contributions</span>
                `
            }
            document.getElementById('contributorview').appendChild(div)
            idx += 1
        }
    })()
</script>

## Top 30 nodecg-io contributors

<div id="contributorview" style="display: grid">

</div>
