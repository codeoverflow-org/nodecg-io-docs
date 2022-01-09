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
[<u>nodecg-io-core] as nodecg_io_core <<core>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/nodecg-io-core]]
[<u>ajv] as ajv <<lib>> [[https://www.npmjs.com/package/ajv]]
[<u>crypto-js] as crypto_js <<lib>> [[https://www.npmjs.com/package/crypto-js]]
[<u>tslib] as tslib <<lib>> [[https://www.npmjs.com/package/tslib]]
[<u>nodecg-io-ahk] as services_nodecg_io_ahk <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-ahk]]
[<u>node-fetch] as node_fetch <<lib>> [[https://www.npmjs.com/package/node-fetch]]
[<u>nodecg-io-android] as services_nodecg_io_android <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-android]]
[<u>@rauschma/stringio] as rauschma_stringio <<lib>> [[https://www.npmjs.com/package/@rauschma/stringio]]
[<u>get-stream] as get_stream <<lib>> [[https://www.npmjs.com/package/get-stream]]
[<u>nodecg-io-artnet] as services_nodecg_io_artnet <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-artnet]]
[<u>artnet-protocol] as artnet_protocol <<lib>> [[https://www.npmjs.com/package/artnet-protocol]]
[<u>nodecg-io-atem] as services_nodecg_io_atem <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-atem]]
[<u>atem-connection] as atem_connection <<lib>> [[https://www.npmjs.com/package/atem-connection]]
[<u>nodecg-io-curseforge] as services_nodecg_io_curseforge <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-curseforge]]
[<u>nodecg-io-dbus] as services_nodecg_io_dbus <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-dbus]]
[<u>dbus-next] as dbus_next <<lib>> [[https://www.npmjs.com/package/dbus-next]]
[<u>nodecg-io-debug] as services_nodecg_io_debug <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-debug]]
[<u>nodecg-types] as nodecg_types <<lib>> [[https://www.npmjs.com/package/nodecg-types]]
[<u>nodecg-io-discord] as services_nodecg_io_discord <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-discord]]
[<u>discord.js] as discord_js <<lib>> [[https://www.npmjs.com/package/discord.js]]
[<u>nodecg-io-discord-rpc] as services_nodecg_io_discord_rpc <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-discord-rpc]]
[<u>discord-rpc] as discord_rpc <<lib>> [[https://www.npmjs.com/package/discord-rpc]]
[<u>@types/discord-rpc] as types_discord_rpc <<lib>> [[https://www.npmjs.com/package/@types/discord-rpc]]
[<u>nodecg-io-elgato-light] as services_nodecg_io_elgato_light <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-elgato-light]]
[<u>@types/node-fetch] as types_node_fetch <<lib>> [[https://www.npmjs.com/package/@types/node-fetch]]
[<u>nodecg-io-github] as services_nodecg_io_github <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-github]]
[<u>@octokit/rest] as octokit_rest <<lib>> [[https://www.npmjs.com/package/@octokit/rest]]
[<u>nodecg-io-googleapis] as services_nodecg_io_googleapis <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-googleapis]]
[<u>@types/gapi] as types_gapi <<lib>> [[https://www.npmjs.com/package/@types/gapi]]
[<u>googleapis] as googleapis <<lib>> [[https://www.npmjs.com/package/googleapis]]
[<u>open] as open <<lib>> [[https://www.npmjs.com/package/open]]
[<u>nodecg-io-intellij] as services_nodecg_io_intellij <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-intellij]]
[<u>nodecg-io-irc] as services_nodecg_io_irc <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-irc]]
[<u>@types/irc] as types_irc <<lib>> [[https://www.npmjs.com/package/@types/irc]]
[<u>irc] as irc <<lib>> [[https://www.npmjs.com/package/irc]]
[<u>nodecg-io-midi-input] as services_nodecg_io_midi_input <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-midi-input]]
[<u>easymidi] as easymidi <<lib>> [[https://www.npmjs.com/package/easymidi]]
[<u>nodecg-io-midi-output] as services_nodecg_io_midi_output <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-midi-output]]
[<u>nodecg-io-mqtt-client] as services_nodecg_io_mqtt_client <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-mqtt-client]]
[<u>mqtt] as mqtt <<lib>> [[https://www.npmjs.com/package/mqtt]]
[<u>nodecg-io-nanoleaf] as services_nodecg_io_nanoleaf <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-nanoleaf]]
[<u>nodecg-io-obs] as services_nodecg_io_obs <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-obs]]
[<u>obs-websocket-js] as obs_websocket_js <<lib>> [[https://www.npmjs.com/package/obs-websocket-js]]
[<u>nodecg-io-philipshue] as services_nodecg_io_philipshue <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-philipshue]]
[<u>is-ip] as is_ip <<lib>> [[https://www.npmjs.com/package/is-ip]]
[<u>node-hue-api] as node_hue_api <<lib>> [[https://www.npmjs.com/package/node-hue-api]]
[<u>nodecg-io-rcon] as services_nodecg_io_rcon <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-rcon]]
[<u>rcon-client] as rcon_client <<lib>> [[https://www.npmjs.com/package/rcon-client]]
[<u>nodecg-io-reddit] as services_nodecg_io_reddit <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-reddit]]
[<u>reddit-ts] as reddit_ts <<lib>> [[https://www.npmjs.com/package/reddit-ts]]
[<u>nodecg-io-sacn-receiver] as services_nodecg_io_sacn_receiver <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-sacn-receiver]]
[<u>sacn] as sacn <<lib>> [[https://www.npmjs.com/package/sacn]]
[<u>nodecg-io-sacn-sender] as services_nodecg_io_sacn_sender <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-sacn-sender]]
[<u>nodecg-io-serial] as services_nodecg_io_serial <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-serial]]
[<u>@serialport/parser-readline] as serialport_parser_readline <<lib>> [[https://www.npmjs.com/package/@serialport/parser-readline]]
[<u>@types/serialport] as types_serialport <<lib>> [[https://www.npmjs.com/package/@types/serialport]]
[<u>serialport] as serialport <<lib>> [[https://www.npmjs.com/package/serialport]]
[<u>nodecg-io-shlink] as services_nodecg_io_shlink <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-shlink]]
[<u>shlink-client] as shlink_client <<lib>> [[https://www.npmjs.com/package/shlink-client]]
[<u>nodecg-io-slack] as services_nodecg_io_slack <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-slack]]
[<u>@slack/web-api] as slack_web_api <<lib>> [[https://www.npmjs.com/package/@slack/web-api]]
[<u>nodecg-io-spotify] as services_nodecg_io_spotify <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-spotify]]
[<u>@types/spotify-web-api-node] as types_spotify_web_api_node <<lib>> [[https://www.npmjs.com/package/@types/spotify-web-api-node]]
[<u>spotify-web-api-node] as spotify_web_api_node <<lib>> [[https://www.npmjs.com/package/spotify-web-api-node]]
[<u>nodecg-io-sql] as services_nodecg_io_sql <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-sql]]
[<u>knex] as knex <<lib>> [[https://www.npmjs.com/package/knex]]
[<u>nodecg-io-streamdeck] as services_nodecg_io_streamdeck <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-streamdeck]]
[<u>@elgato-stream-deck/node] as elgato_stream_deck_node <<lib>> [[https://www.npmjs.com/package/@elgato-stream-deck/node]]
[<u>nodecg-io-streamelements] as services_nodecg_io_streamelements <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-streamelements]]
[<u>@types/socket.io-client] as types_socket_io_client <<lib>> [[https://www.npmjs.com/package/@types/socket.io-client]]
[<u>socket.io-client] as socket_io_client <<lib>> [[https://www.npmjs.com/package/socket.io-client]]
[<u>nodecg-io-telegram] as services_nodecg_io_telegram <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-telegram]]
[<u>@types/node-telegram-bot-api] as types_node_telegram_bot_api <<lib>> [[https://www.npmjs.com/package/@types/node-telegram-bot-api]]
[<u>node-telegram-bot-api] as node_telegram_bot_api <<lib>> [[https://www.npmjs.com/package/node-telegram-bot-api]]
[<u>nodecg-io-template] as services_nodecg_io_template <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-template]]
[<u>nodecg-io-tiane] as services_nodecg_io_tiane <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-tiane]]
[<u>ws] as ws <<lib>> [[https://www.npmjs.com/package/ws]]
[<u>nodecg-io-twitch-addons] as services_nodecg_io_twitch_addons <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-twitch-addons]]
[<u>nodecg-io-twitch-auth] as nodecg_io_twitch_auth <<lib>> [[https://www.npmjs.com/package/nodecg-io-twitch-auth]]
[<u>nodecg-io-twitch-api] as services_nodecg_io_twitch_api <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-twitch-api]]
[<u>@twurple/api] as twurple_api <<lib>> [[https://www.npmjs.com/package/@twurple/api]]
[<u>nodecg-io-twitch-chat] as services_nodecg_io_twitch_chat <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-twitch-chat]]
[<u>@twurple/chat] as twurple_chat <<lib>> [[https://www.npmjs.com/package/@twurple/chat]]
[<u>nodecg-io-twitch-pubsub] as services_nodecg_io_twitch_pubsub <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-twitch-pubsub]]
[<u>@twurple/pubsub] as twurple_pubsub <<lib>> [[https://www.npmjs.com/package/@twurple/pubsub]]
[<u>nodecg-io-twitter] as services_nodecg_io_twitter <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-twitter]]
[<u>@types/twitter] as types_twitter <<lib>> [[https://www.npmjs.com/package/@types/twitter]]
[<u>twitter] as twitter <<lib>> [[https://www.npmjs.com/package/twitter]]
[<u>nodecg-io-websocket-client] as services_nodecg_io_websocket_client <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-websocket-client]]
[<u>@types/ws] as types_ws <<lib>> [[https://www.npmjs.com/package/@types/ws]]
[<u>nodecg-io-websocket-server] as services_nodecg_io_websocket_server <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-websocket-server]]
[<u>nodecg-io-xdotool] as services_nodecg_io_xdotool <<service>> [[https://github.com/codeoverflow-org/nodecg-io/tree/main/services/nodecg-io-xdotool]]
nodecg_io_core ...> ajv
nodecg_io_core ...> crypto_js
nodecg_io_core ...> tslib
services_nodecg_io_ahk ...> node_fetch
services_nodecg_io_ahk --> nodecg_io_core
services_nodecg_io_android ...> rauschma_stringio
services_nodecg_io_android ...> get_stream
services_nodecg_io_android --> nodecg_io_core
services_nodecg_io_artnet --> nodecg_io_core
services_nodecg_io_artnet ...> artnet_protocol
services_nodecg_io_atem ...> atem_connection
services_nodecg_io_atem --> nodecg_io_core
services_nodecg_io_curseforge ...> node_fetch
services_nodecg_io_curseforge --> nodecg_io_core
services_nodecg_io_dbus --> nodecg_io_core
services_nodecg_io_dbus ...> dbus_next
services_nodecg_io_debug --> nodecg_io_core
services_nodecg_io_debug ...> nodecg_types
services_nodecg_io_discord ...> discord_js
services_nodecg_io_discord --> nodecg_io_core
services_nodecg_io_discord_rpc --> nodecg_io_core
services_nodecg_io_discord_rpc ...> discord_rpc
services_nodecg_io_discord_rpc ...> types_discord_rpc
services_nodecg_io_discord_rpc ...> node_fetch
services_nodecg_io_elgato_light ...> types_node_fetch
services_nodecg_io_elgato_light ...> node_fetch
services_nodecg_io_elgato_light --> nodecg_io_core
services_nodecg_io_github --> nodecg_io_core
services_nodecg_io_github ...> octokit_rest
services_nodecg_io_googleapis ...> types_gapi
services_nodecg_io_googleapis ...> googleapis
services_nodecg_io_googleapis --> nodecg_io_core
services_nodecg_io_googleapis ...> open
services_nodecg_io_intellij ...> node_fetch
services_nodecg_io_intellij --> nodecg_io_core
services_nodecg_io_irc ...> types_irc
services_nodecg_io_irc ...> irc
services_nodecg_io_irc --> nodecg_io_core
services_nodecg_io_midi_input ...> easymidi
services_nodecg_io_midi_input --> nodecg_io_core
services_nodecg_io_midi_output ...> easymidi
services_nodecg_io_midi_output --> nodecg_io_core
services_nodecg_io_mqtt_client --> nodecg_io_core
services_nodecg_io_mqtt_client ...> mqtt
services_nodecg_io_nanoleaf ...> types_node_fetch
services_nodecg_io_nanoleaf ...> node_fetch
services_nodecg_io_nanoleaf --> nodecg_io_core
services_nodecg_io_nanoleaf ...> nodecg_types
services_nodecg_io_obs --> nodecg_io_core
services_nodecg_io_obs ...> obs_websocket_js
services_nodecg_io_philipshue ...> is_ip
services_nodecg_io_philipshue ...> node_hue_api
services_nodecg_io_philipshue --> nodecg_io_core
services_nodecg_io_rcon --> nodecg_io_core
services_nodecg_io_rcon ...> rcon_client
services_nodecg_io_reddit --> nodecg_io_core
services_nodecg_io_reddit ...> reddit_ts
services_nodecg_io_sacn_receiver --> nodecg_io_core
services_nodecg_io_sacn_receiver ...> sacn
services_nodecg_io_sacn_sender --> nodecg_io_core
services_nodecg_io_sacn_sender ...> sacn
services_nodecg_io_serial ...> serialport_parser_readline
services_nodecg_io_serial ...> types_serialport
services_nodecg_io_serial --> nodecg_io_core
services_nodecg_io_serial ...> serialport
services_nodecg_io_shlink --> nodecg_io_core
services_nodecg_io_shlink ...> shlink_client
services_nodecg_io_slack ...> slack_web_api
services_nodecg_io_slack --> nodecg_io_core
services_nodecg_io_spotify ...> types_spotify_web_api_node
services_nodecg_io_spotify --> nodecg_io_core
services_nodecg_io_spotify ...> open
services_nodecg_io_spotify ...> spotify_web_api_node
services_nodecg_io_sql ...> knex
services_nodecg_io_sql --> nodecg_io_core
services_nodecg_io_streamdeck ...> elgato_stream_deck_node
services_nodecg_io_streamdeck --> nodecg_io_core
services_nodecg_io_streamelements ...> types_socket_io_client
services_nodecg_io_streamelements --> nodecg_io_core
services_nodecg_io_streamelements ...> socket_io_client
services_nodecg_io_telegram ...> types_node_telegram_bot_api
services_nodecg_io_telegram ...> node_telegram_bot_api
services_nodecg_io_telegram --> nodecg_io_core
services_nodecg_io_template --> nodecg_io_core
services_nodecg_io_tiane --> nodecg_io_core
services_nodecg_io_tiane ...> ws
services_nodecg_io_twitch_addons ...> node_fetch
services_nodecg_io_twitch_addons --> nodecg_io_core
services_nodecg_io_twitch_addons ...> nodecg_io_twitch_auth
services_nodecg_io_twitch_api --> nodecg_io_core
services_nodecg_io_twitch_api ...> nodecg_io_twitch_auth
services_nodecg_io_twitch_api ...> twurple_api
services_nodecg_io_twitch_chat --> nodecg_io_core
services_nodecg_io_twitch_chat ...> nodecg_io_twitch_auth
services_nodecg_io_twitch_chat ...> twurple_chat
services_nodecg_io_twitch_pubsub --> nodecg_io_core
services_nodecg_io_twitch_pubsub ...> nodecg_io_twitch_auth
services_nodecg_io_twitch_pubsub ...> twurple_api
services_nodecg_io_twitch_pubsub ...> twurple_pubsub
services_nodecg_io_twitter ...> types_twitter
services_nodecg_io_twitter --> nodecg_io_core
services_nodecg_io_twitter ...> twitter
services_nodecg_io_websocket_client ...> types_ws
services_nodecg_io_websocket_client --> nodecg_io_core
services_nodecg_io_websocket_client ...> ws
services_nodecg_io_websocket_server ...> types_ws
services_nodecg_io_websocket_server --> nodecg_io_core
services_nodecg_io_websocket_server ...> ws
services_nodecg_io_xdotool ...> rauschma_stringio
services_nodecg_io_xdotool ...> node_fetch
services_nodecg_io_xdotool --> nodecg_io_core
::end-uml::
