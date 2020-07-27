<style>
    a.contributorlink:hover {
        text-decoration-style: solid;
        text-decoration-line: underline;
        text-decoration-color: white;
    }
</style>

<script type="text/javascript">
    fetch('https://api.github.com/repos/codeoverflow-org/nodecg-io/contributors').then(response => {
        response.json().then(data => {
            let idx = 1
            data.forEach(entry => {
                const div = document.createElement('div')
                div.style = `grid-column: 1; grid-row: ${idx}; display: inline-block; padding-bottom: 10px`
                if ('avatar_url' in entry) {
                    div.innerHTML = `
                    <img src="${entry.avatar_url}" width="64" height="64" style="float: left; margin-top: 0">
                    <div style="float:left; margin-top: 0">
                      <span style="font-size: 16pt; font-weight: bold; margin-left: 1em; color: white;">
                        <a style="color: white;" class="contributorlink" href="${entry.html_url}">${entry.login}</a>
                      </span><br>
                      <span style="font-size: 12pt; margin-left: 1em; color: white;">
                        <a style="color: white;" class="contributorlink" href="https://github.com/codeoverflow-org/nodecg-io/commits?author=${entry.login}">${entry.contributions} contributions</a>
                      </span>
                    </div>
                    `
                } else {
                    div.innerHTML = `
                    <span style="font-size: 16pt; font-weight: bold; margin-left: 1em; color: white;">${entry.login}</span><br>
                    <span style="font-size: 12pt; margin-left: 1em; color: white;">${entry.contributions} contributions</span>
                    `
                }
                document.getElementById('contributorview').appendChild(div)
                idx += 1
            })
        })
    })
</script>

## Top 30 nodecg-io contributors

<div id="contributorview" style="display: grid">

</div>