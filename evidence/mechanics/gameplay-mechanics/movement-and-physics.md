# Movement and Physics

## Climbing without Climbing

By: Nitley\#3485  
Addded: 04/05/2021

**Finding:** After familiarizing myself with the technique of b-hopping in the first week of Genshin's official release for the purpose of re-roll AR7 speedruns, this would quickly become my exclusive means of travel. This led me to discover an alternative faster method of scaling near-vertical walls \(without climbing or consuming stamina at all\).

**Evidence:**

* [Introduction to b-hopping by Arch- er](https://youtu.be/3bY_vUgHY_g)
* [Climbing without Climbing](https://youtu.be/n56JICDn1Eg)

**Significance:** Can make virtually any travel quicker, whether you're mob farming around your world, crystal farming, or getting character ascension mats etc etc..

## Movement Techniques and Player Model Comparisons

By: Nitley\#3485 and Kourinn\#6001  
Added: 04/10/2021

**Theory:** What is the fastest movement technique for both short distances and long distances? Do movement speed buffs produce non-linear scaling for different character model sizes?

* Short Distance = The distance you're able to sprint with 1 full bar of stamina \(assuming 240 max\).
* Long Distance = The distance traveled by sprinting with a full bar of stamina and continued travel until complete stamina regen.

**Evidence:** TIme stamps available in spreadsheet + video descriptions

* [Google spreadsheet](https://docs.google.com/spreadsheets/d/e/2PACX-1vRmNrVjMuBzcJGQeKzMhUKglJjJocONdBhOeL83McT9Kfrn8_XlN6DUqPmfI1RmJFa7pluM--IqT-Wd/pubhtml) of recorded times
* [Short Distance](https://youtu.be/oJH8cS1SnRY)
* [Long Distance](https://youtu.be/ySDRLkYP8sk)

**Significance:** 

The fastest movement technique for a short distance is to chain dashes together with equal spacing between them with an adult male as they have the biggest strides. This will ensure your dash has more uptime than simply dash spamming. For long-distance you will do the same, dash chaining with maximum dash uptime on an adult male then switching to a teen male for the last dash of your stamina charge and chaining b-hops from thereon.

Demonstration: [Youtube](https://youtu.be/H950uTOSTQs)

A 10% movement speed buff does not cause b-hopping with other model types to be faster than a teen male with the same buff. However, I am still yet to test 20%/20% effects although not expected to change either.

**The Math:** Comes to the same conclusions as the empirical tests above.

```python
Stamina Cost Reduction

Anemo Resonance : 15%
Kaeya Passive   : 20%
Food            : 25%
                   =
Total           : 50%

===

Base dash stamina cost : 15
Effective stamina cost : 7.5 (after Stamina Cost Reduction)

Stamina capacity           : 240
Effective stamina capacity : 225 (cannot dash at/below 15 stamina regardless of stamina cost reductions)

Stamina regen delay : 1 sec
Stamina regen rate  : 30/sec


Full stamina dash count: 225/7.5 = 30
Full stamina regen duration: 1s + (225/30)s = 8.5s
not-sprinting test = sprinting * 1.3 = 15:45 (needs more testing to verify)

===

velocity = distance / time

v(b-hop)      = 1000 d / 9:47 f = 1.7035775127768313 d/f
v(dash-chain) = 1000 d / 9:12 f = 1.8115942028985508 d/f
v(not-sprint) = 1000 d / 15:45 f = 1.0582010582010581 d/f

===

distance = velocity * time

30s * v(dash-chain) + 8.5s * v(not-sprint) = 63.34253508166552 d
38.5s * v(b-hop)                           = 65.58773424190801 d
```

B-Hopping should be 3.5% faster than dash-chaining, waiting for full stamina, and repeating.

