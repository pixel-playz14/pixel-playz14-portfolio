# chatgames
function chatgames():
  delete {chatgame::*}
  set {_i} to integer between 1 and 5:
    if {_i} = 1:
      set {chatgame::answer} to "minecraft"
      set {chatgame::scramble} to "inemcrtaf"
    if {_i} = 2:
      set {chatgame::answer} to "pixel"
      set {chatgame::scramble} to "lexip"
    if {_i} = 3:
      set {chatgame::answer} to "tyler"
      set {chatgame::scramble} to "relyt"
    if {_i} = 4:
      set {chatgame::answer} to "title"
      set {chatgame::scramble} to "tliet"
    if {_i} = 5:
      set {chatgame::answer} to "server"
      set {chatgame::scramble} to "svreer"
    broadcast "first to unscramble %{chatgame::scramble}% wins a prize"
    wait 20 seconds
    if {chatgame::*} is set:
      broadcast "&cno one got it the answer was ''%{chatgame::answer}%''"
every 5 minutes:
  chatgames()
every 1 second:
  if {chatgame::*} is set:
    add 0.1 seconds to {chatgame::timer}
on chat:
  if {chatgame::*} is set:
    set {_msg} to message
    if {_msg} is {chatgame::answer}:
      broadcast "%player% got ''%{chatgame::answer}%'' in %{chatgame::timer}%"
