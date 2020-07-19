<!-- This file is auto-generated. Do not change anything here -->
# Dependency Graph

::uml:: format="svg_inline" classes="uml" alt="PlantUML dependency graph" title="PlantUML dependency graph"
left to right direction
skinparam HyperlinkColor White
skinparam component {
ArrowColor Gainsboro
BackgroundColor<<core>> Crimson
BackgroundColor<<service>> Darkorange
BackgroundColor<<lib>> GoldenRod
BorderColor Black
FontColor White
FontStyle Underline
}
[<u>nodecg-io-core] as nodecg_io_core <<core>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-core]]
[<u>ajv] as ajv <<lib>> [[https://www.npmjs.com/package/ajv]]
[<u>crypto-js] as crypto_js <<lib>> [[https://www.npmjs.com/package/crypto-js]]
[<u>tslib] as tslib <<lib>> [[https://www.npmjs.com/package/tslib]]
[<u>typescript] as typescript <<lib>> [[https://www.npmjs.com/package/typescript]]
[<u>nodecg-io-ahk] as nodecg_io_ahk <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-ahk]]
[<u>node-fetch] as node_fetch <<lib>> [[https://www.npmjs.com/package/node-fetch]]
[<u>nodecg-io-discord] as nodecg_io_discord <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-discord]]
[<u>discord.js] as discord_js <<lib>> [[https://www.npmjs.com/package/discord.js]]
[<u>nodecg-io-intellij] as nodecg_io_intellij <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-intellij]]
[<u>nodecg-io-irc] as nodecg_io_irc <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-irc]]
[<u>irc] as irc <<lib>> [[https://www.npmjs.com/package/irc]]
[<u>nodecg-io-midi-input] as nodecg_io_midi_input <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-midi-input]]
[<u>easymidi] as easymidi <<lib>> [[https://www.npmjs.com/package/easymidi]]
[<u>nodecg-io-midi-output] as nodecg_io_midi_output <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-midi-output]]
[<u>nodecg-io-philipshue] as nodecg_io_philipshue <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-philipshue]]
[<u>is-ip] as is_ip <<lib>> [[https://www.npmjs.com/package/is-ip]]
[<u>node-hue-api] as node_hue_api <<lib>> [[https://www.npmjs.com/package/node-hue-api]]
[<u>nodecg-io-rcon] as nodecg_io_rcon <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-rcon]]
[<u>rcon-client] as rcon_client <<lib>> [[https://www.npmjs.com/package/rcon-client]]
[<u>nodecg-io-slack] as nodecg_io_slack <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-slack]]
[<u>@slack/web-api] as slack_web_api <<lib>> [[https://www.npmjs.com/package/@slack/web-api]]
[<u>nodecg-io-spotify] as nodecg_io_spotify <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-spotify]]
[<u>open] as open <<lib>> [[https://www.npmjs.com/package/open]]
[<u>spotify-web-api-node] as spotify_web_api_node <<lib>> [[https://www.npmjs.com/package/spotify-web-api-node]]
[<u>nodecg-io-streamdeck] as nodecg_io_streamdeck <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-streamdeck]]
[<u>elgato-stream-deck] as elgato_stream_deck <<lib>> [[https://www.npmjs.com/package/elgato-stream-deck]]
[<u>nodecg-io-twitch] as nodecg_io_twitch <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-twitch]]
[<u>twitch] as twitch <<lib>> [[https://www.npmjs.com/package/twitch]]
[<u>twitch-chat-client] as twitch_chat_client <<lib>> [[https://www.npmjs.com/package/twitch-chat-client]]
[<u>nodecg-io-twitter] as nodecg_io_twitter <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-twitter]]
[<u>@types/twitter] as types_twitter <<lib>> [[https://www.npmjs.com/package/@types/twitter]]
[<u>twitter] as twitter <<lib>> [[https://www.npmjs.com/package/twitter]]
[<u>nodecg-io-ws-client] as nodecg_io_ws_client <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-ws-client]]
[<u>@types/ws] as types_ws <<lib>> [[https://www.npmjs.com/package/@types/ws]]
[<u>ws] as ws <<lib>> [[https://www.npmjs.com/package/ws]]
[<u>nodecg-io-ws-server] as nodecg_io_ws_server <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-ws-server]]
[<u>nodecg-io-xdotool] as nodecg_io_xdotool <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-xdotool]]
[<u>@rauschma/stringio] as rauschma_stringio <<lib>> [[https://www.npmjs.com/package/@rauschma/stringio]]
nodecg_io_core ...> ajv
nodecg_io_core ...> crypto_js
nodecg_io_core ...> tslib
nodecg_io_core ...> typescript
nodecg_io_ahk --> nodecg_io_core
nodecg_io_ahk ...> node_fetch
nodecg_io_discord --> nodecg_io_core
nodecg_io_discord ...> discord_js
nodecg_io_intellij --> nodecg_io_core
nodecg_io_intellij ...> node_fetch
nodecg_io_irc --> nodecg_io_core
nodecg_io_irc ...> irc
nodecg_io_midi_input --> nodecg_io_core
nodecg_io_midi_input ...> easymidi
nodecg_io_midi_output --> nodecg_io_core
nodecg_io_midi_output ...> easymidi
nodecg_io_philipshue ...> is_ip
nodecg_io_philipshue ...> node_hue_api
nodecg_io_philipshue --> nodecg_io_core
nodecg_io_rcon --> nodecg_io_core
nodecg_io_rcon ...> rcon_client
nodecg_io_slack --> nodecg_io_core
nodecg_io_slack ...> slack_web_api
nodecg_io_spotify --> nodecg_io_core
nodecg_io_spotify ...> open
nodecg_io_spotify ...> spotify_web_api_node
nodecg_io_streamdeck --> nodecg_io_core
nodecg_io_streamdeck ...> elgato_stream_deck
nodecg_io_twitch --> nodecg_io_core
nodecg_io_twitch ...> twitch
nodecg_io_twitch ...> twitch_chat_client
nodecg_io_twitter ...> types_twitter
nodecg_io_twitter --> nodecg_io_core
nodecg_io_twitter ...> twitter
nodecg_io_ws_client --> nodecg_io_core
nodecg_io_ws_client ...> types_ws
nodecg_io_ws_client ...> ws
nodecg_io_ws_server --> nodecg_io_core
nodecg_io_ws_server ...> types_ws
nodecg_io_ws_server ...> ws
nodecg_io_xdotool --> nodecg_io_core
nodecg_io_xdotool ...> node_fetch
nodecg_io_xdotool ...> rauschma_stringio
::end-uml::
