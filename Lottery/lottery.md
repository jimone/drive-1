## 抽奖公共接口
抽奖接口在LotteryModel下
```
public function  GetPrize ()   //传入openid 活动id 判断此用户是否中奖，并返回相应奖品
参数：
array('openid' =>  ,  //用户openid
'weight' => ,  //传入权重 默认为1
'activity_id' => )   // 活动id

public function SetPeizt ()   // 传入openid prize_id 获奖数量（红包金额）默认为1 num
参数：
array(
  'openid' =>
  'prize_id' => 
  'num' => 
)
```
