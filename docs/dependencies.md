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
[<u>@types/irc] as types_irc <<lib>> [[https://www.npmjs.com/package/@types/irc]]
[<u>irc] as irc <<lib>> [[https://www.npmjs.com/package/irc]]
[<u>nodecg-io-midi-input] as nodecg_io_midi_input <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-midi-input]]
[<u>easymidi] as easymidi <<lib>> [[https://www.npmjs.com/package/easymidi]]
[<u>nodecg-io-midi-output] as nodecg_io_midi_output <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-midi-output]]
[<u>nodecg-io-obs] as nodecg_io_obs <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-obs]]
[<u>obs-websocket-js] as obs_websocket_js <<lib>> [[https://www.npmjs.com/package/obs-websocket-js]]
[<u>nodecg-io-philipshue] as nodecg_io_philipshue <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-philipshue]]
[<u>is-ip] as is_ip <<lib>> [[https://www.npmjs.com/package/is-ip]]
[<u>node-hue-api] as node_hue_api <<lib>> [[https://www.npmjs.com/package/node-hue-api]]
[<u>nodecg-io-rcon] as nodecg_io_rcon <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-rcon]]
[<u>rcon-client] as rcon_client <<lib>> [[https://www.npmjs.com/package/rcon-client]]
[<u>nodecg-io-reddit] as nodecg_io_reddit <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-reddit]]
[<u>reddit-ts] as reddit_ts <<lib>> [[https://www.npmjs.com/package/reddit-ts]]
[<u>nodecg-io-sacn-receiver] as nodecg_io_sacn_receiver <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-sacn-receiver]]
[<u>sacn] as sacn <<lib>> [[https://www.npmjs.com/package/sacn]]
[<u>nodecg-io-sacn-sender] as nodecg_io_sacn_sender <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-sacn-sender]]
[<u>nodecg-io-serial] as nodecg_io_serial <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-serial]]
[<u>@types/serialport] as types_serialport <<lib>> [[https://www.npmjs.com/package/@types/serialport]]
[<u>@serialport/parser-readline] as serialport_parser_readline <<lib>> [[https://www.npmjs.com/package/@serialport/parser-readline]]
[<u>serialport] as serialport <<lib>> [[https://www.npmjs.com/package/serialport]]
[<u>nodecg-io-slack] as nodecg_io_slack <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-slack]]
[<u>@slack/web-api] as slack_web_api <<lib>> [[https://www.npmjs.com/package/@slack/web-api]]
[<u>nodecg-io-spotify] as nodecg_io_spotify <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-spotify]]
[<u>@types/spotify-web-api-node] as types_spotify_web_api_node <<lib>> [[https://www.npmjs.com/package/@types/spotify-web-api-node]]
[<u>express] as express <<lib>> [[https://www.npmjs.com/package/express]]
[<u>open] as open <<lib>> [[https://www.npmjs.com/package/open]]
[<u>spotify-web-api-node] as spotify_web_api_node <<lib>> [[https://www.npmjs.com/package/spotify-web-api-node]]
[<u>nodecg-io-streamdeck] as nodecg_io_streamdeck <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-streamdeck]]
[<u>elgato-stream-deck] as elgato_stream_deck <<lib>> [[https://www.npmjs.com/package/elgato-stream-deck]]
[<u>nodecg-io-streamelements] as nodecg_io_streamelements <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-streamelements]]
[<u>@types/socket.io-client] as types_socket_io_client <<lib>> [[https://www.npmjs.com/package/@types/socket.io-client]]
[<u>socket.io-client] as socket_io_client <<lib>> [[https://www.npmjs.com/package/socket.io-client]]
[<u>nodecg-io-telegram] as nodecg_io_telegram <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-telegram]]
[<u>@types/node-telegram-bot-api] as types_node_telegram_bot_api <<lib>> [[https://www.npmjs.com/package/@types/node-telegram-bot-api]]
[<u>node-telegram-bot-api] as node_telegram_bot_api <<lib>> [[https://www.npmjs.com/package/node-telegram-bot-api]]
[<u>nodecg-io-tiane] as nodecg_io_tiane <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-tiane]]
[<u>ws] as ws <<lib>> [[https://www.npmjs.com/package/ws]]
[<u>nodecg-io-twitch-chat] as nodecg_io_twitch_chat <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-twitch-chat]]
[<u>twitch] as twitch <<lib>> [[https://www.npmjs.com/package/twitch]]
[<u>twitch-auth] as twitch_auth <<lib>> [[https://www.npmjs.com/package/twitch-auth]]
[<u>twitch-chat-client] as twitch_chat_client <<lib>> [[https://www.npmjs.com/package/twitch-chat-client]]
[<u>nodecg-io-twitch-pubsub] as nodecg_io_twitch_pubsub <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-twitch-pubsub]]
[<u>twitch-pubsub-client] as twitch_pubsub_client <<lib>> [[https://www.npmjs.com/package/twitch-pubsub-client]]
[<u>nodecg-io-twitter] as nodecg_io_twitter <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-twitter]]
[<u>@types/twitter] as types_twitter <<lib>> [[https://www.npmjs.com/package/@types/twitter]]
[<u>twitter] as twitter <<lib>> [[https://www.npmjs.com/package/twitter]]
[<u>nodecg-io-websocket-client] as nodecg_io_websocket_client <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-websocket-client]]
[<u>@types/ws] as types_ws <<lib>> [[https://www.npmjs.com/package/@types/ws]]
[<u>nodecg-io-websocket-server] as nodecg_io_websocket_server <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-websocket-server]]
[<u>nodecg-io-xdotool] as nodecg_io_xdotool <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-xdotool]]
[<u>@rauschma/stringio] as rauschma_stringio <<lib>> [[https://www.npmjs.com/package/@rauschma/stringio]]
[<u>nodecg-io-youtube] as nodecg_io_youtube <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/master/nodecg-io-youtube]]
[<u>@types/gapi] as types_gapi <<lib>> [[https://www.npmjs.com/package/@types/gapi]]
[<u>googleapis] as googleapis <<lib>> [[https://www.npmjs.com/package/googleapis]]
nodecg_io_core ...> ajv
nodecg_io_core ...> crypto_js
nodecg_io_core ...> tslib
nodecg_io_core ...> typescript
nodecg_io_ahk --> nodecg_io_core
nodecg_io_ahk ...> node_fetch
nodecg_io_discord ...> discord_js
nodecg_io_discord --> nodecg_io_core
nodecg_io_intellij --> nodecg_io_core
nodecg_io_intellij ...> node_fetch
nodecg_io_irc ...> types_irc
nodecg_io_irc ...> irc
nodecg_io_irc --> nodecg_io_core
nodecg_io_midi_input --> nodecg_io_core
nodecg_io_midi_input ...> easymidi
nodecg_io_midi_output --> nodecg_io_core
nodecg_io_midi_output ...> easymidi
nodecg_io_obs --> nodecg_io_core
nodecg_io_obs ...> obs_websocket_js
nodecg_io_philipshue ...> is_ip
nodecg_io_philipshue ...> node_hue_api
nodecg_io_philipshue --> nodecg_io_core
nodecg_io_rcon --> nodecg_io_core
nodecg_io_rcon ...> rcon_client
nodecg_io_reddit --> nodecg_io_core
nodecg_io_reddit ...> reddit_ts
nodecg_io_sacn_receiver --> nodecg_io_core
nodecg_io_sacn_receiver ...> sacn
nodecg_io_sacn_sender --> nodecg_io_core
nodecg_io_sacn_sender ...> sacn
nodecg_io_serial ...> types_serialport
nodecg_io_serial ...> serialport_parser_readline
nodecg_io_serial --> nodecg_io_core
nodecg_io_serial ...> serialport
nodecg_io_slack ...> slack_web_api
nodecg_io_slack --> nodecg_io_core
nodecg_io_spotify ...> types_spotify_web_api_node
nodecg_io_spotify ...> express
nodecg_io_spotify --> nodecg_io_core
nodecg_io_spotify ...> open
nodecg_io_spotify ...> spotify_web_api_node
nodecg_io_streamdeck ...> elgato_stream_deck
nodecg_io_streamdeck --> nodecg_io_core
nodecg_io_streamelements ...> types_socket_io_client
nodecg_io_streamelements --> nodecg_io_core
nodecg_io_streamelements ...> socket_io_client
nodecg_io_telegram ...> types_node_telegram_bot_api
nodecg_io_telegram ...> node_telegram_bot_api
nodecg_io_telegram --> nodecg_io_core
nodecg_io_tiane --> nodecg_io_core
nodecg_io_tiane ...> ws
nodecg_io_twitch_chat --> nodecg_io_core
nodecg_io_twitch_chat ...> twitch
nodecg_io_twitch_chat ...> twitch_auth
nodecg_io_twitch_chat ...> twitch_chat_client
nodecg_io_twitch_pubsub --> nodecg_io_core
nodecg_io_twitch_pubsub ...> twitch
nodecg_io_twitch_pubsub ...> twitch_pubsub_client
nodecg_io_twitter ...> types_twitter
nodecg_io_twitter --> nodecg_io_core
nodecg_io_twitter ...> twitter
nodecg_io_websocket_client ...> types_ws
nodecg_io_websocket_client --> nodecg_io_core
nodecg_io_websocket_client ...> ws
nodecg_io_websocket_server ...> types_ws
nodecg_io_websocket_server --> nodecg_io_core
nodecg_io_websocket_server ...> ws
nodecg_io_xdotool --> nodecg_io_core
nodecg_io_xdotool ...> node_fetch
nodecg_io_xdotool ...> rauschma_stringio
nodecg_io_youtube ...> types_gapi
nodecg_io_youtube ...> express
nodecg_io_youtube ...> googleapis
nodecg_io_youtube --> nodecg_io_core
nodecg_io_youtube ...> open
::end-uml::
