# bos-account

在bos-testnet上部署了创建账号合约signupeoseos

+ 合约创建账号过程：

    通过eosio.token 的transfer动作向signupeoseos转账“2 BOS”，
    其中“0.1 BOS”用户购买CPU，“0.1 BOS”用于购买NET，其余代币用于买ram.
    转账的BOS币数量不一定为2 BOS，但必须大于0.2 BOS
    
+ 创建账号密钥

   `cleos create key --to-console`
   Private key: 5JxkEiiCnYEeS2FYnRgrFEK2Lhxujiy2kFbhNQ382HybaAr1ti5
   Public key: EOS76VqrCpuK5dKsGfGP9aPuxpRTAoJcPMfEknVy47n6xkh6zNRrh
   
+ 合约创建账号

  用已有的BOS 账号 bosboseoseos 创建新账号 boscreator11
  
  eosio.token的transfer, memo: new_account + public key
  
  new_account：boscreator11
  
  publick key: EOS76VqrCpuK5dKsGfGP9aPuxpRTAoJcPMfEknVy47n6xkh6zNRrh
  
  `cleos push action eosio.token transfer '["bosboseoseos","signupeoseos","2 BOS", "boscreator11-EOS76VqrCpuK5dKsGfGP9aPuxpRTAoJcPMfEknVy47n6xkh6zNRrh"]' -p bosboseoseos`


