# -CLEO-Disconnect
{$CLEO .cs}
{$USE Cleo+}
0000: NOP
:1
wait 0 ms
if and
not Samp.ChatInputOpened()
0AB0: key_pressed 18 // left alt
0AB0: key_pressed 82 // R
004D: jump_if_false @1
0B28: samp disconnect_with_reason 0@ // set reconnecting gamestate
0AA5: call 8535003 num_params 3 pop 3 0 0 0
0002: jump @1
