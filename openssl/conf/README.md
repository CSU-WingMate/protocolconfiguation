该协议使用不同的命令参数：

默认：

/usr/local/openssl-3.3.1/bin/openssl s_server -dtls1_2 -cert /opt/openssl-3.3.1/demos/sslecho/cert.pem -key /opt/openssl-3.3.1/demos/sslecho/key.pem -accept 4444

自定义：

  /usr/local/openssl-3.3.1/bin/openssl s_server -dtls1_2 -cert /opt/openssl-3.3.1/demos/sslecho/cert.pem -key /opt/openssl-3.3.1/demos/sslecho/key.pem -accept 4448 -msg -trace -unlink -6 -no-CAfile -no-CApath -no-CAstore -nocert -build_chain -crlf -no_resume_ephemeral -tlsextdebug -crl_download -ext_cache -ign_eof -status
 
  /usr/local/openssl-3.3.1/bin/openssl s_server -dtls1_2 -cert /opt/openssl-3.3.1/demos/sslecho/cert.pem -key /opt/openssl-3.3.1/demos/sslecho/key.pem -accept 4449 -msg -max_send_frag 1024 -split_send_frag 16 -read_buf 24 -mtu 2048 -nbio -naccept 10 -max_pipelines 10 -async
 
  /usr/local/openssl-3.3.1/bin/openssl s_server -dtls1_2 -cert /opt/openssl-3.3.1/demos/sslecho/cert.pem -key /opt/openssl-3.3.1/demos/sslecho/key.pem -accept 4450 -msg -trace -unlink -4 -context "my_session_context" -no-CAfile -no-CApath -no-CAstore -verify 1024  -crlf -no_resume_ephemeral  -tlsextdebug -crl_download -ext_cache -ign_eof -status -nameopt RFC2253,oneline -servername_fatal -nbio_test -crlf -quiet
  
  /usr/local/openssl-3.3.1/bin/openssl  s_server -dtls1_2 -cert /opt/openssl-3.3.1/demos/sslecho/cert.pem -key /opt/openssl-3.3.1/demos/sslecho/key.pem -accept 4451 -msg -max_send_frag 1024 -split_send_frag 1024 -read_buf 2 -mtu 512 -nbio -naccept 1000 -max_pipelines 10 -async -brief -no_ign_eof -verify_return_error -ext_cache -no_cache

