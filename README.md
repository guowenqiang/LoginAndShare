# LoginAndShare
使用友盟分享到微信,QQ,微博等第三方分享和登录注意事项
1 微信昵称和头像修改后,友盟获取到的微信昵称头像等不变,咨询过友盟客服,只有手动切换微信账号才能获取到新的昵称和头像,否则不变
2 微信登录只有第一次出现授权的界面,并且不能切换账号,是因为微信没有多账号功能和网页登录功能,qq和微博等都能通过先删除授权,在调用授权方法来让用户切换账号
删除授权示例: UMShareAPI.get(mActivity).deleteOauth(mActivity, SHARE_MEDIA.QQ, null);
授权示例: UMShareAPI.get(mActivity).doOauthVerify(mActivity, SHARE_MEDIA.SINA, authListener);
