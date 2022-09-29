---
title: "Quote about how to build AI for Big2"
date: 2020-11-08T15:49:00+08:00
draft: false
---

Part of a post on LIHKG which contains an insightful response to my question.

Me:
> 自己想試吓寫一隻同電腦對戰嘅簡陋鋤大D, 但係對點寫AI完全冇idea #xx(#lm2

User "Angular":
> 其實你你想像中咁難，因為其實鋤Dee 啲action 都幾constrainted, 即係人地行單支，你要跟住行單支咁。 你只要跟返你自己鋤Dee嘅strategy 去寫一堆rule 就得，例如行單支嘅，就如果出面張牌細個jack，就係唔拆五張嘅情況吓打最細嗰隻咁
>你可以寫啲function 去evaluate 應唔應該拆五張，pair等，當你話事嗰時，又可以寫嗰function 去evaluation 應該行單支， pair定其他。 呢啲evaluation 可以based on 你對其他對手手牌嘅probability distribution，而呢啲evaluation都係啲optimization problem, 希望揀一個action 去maximize final utility
> 其實你唔係一黎就玩multiplayer imperfect information game 嘅話，而係2 players perfect information game, 你可以睇minimax algorithm, 否則，你可以睇吓reinforced learning 係乜，乜係MDP, value iteration, policy iteration 同Q-learning 先。 deep reinforced learning 都係based on 呢啲嘢，只係replace 咗啲value function/policy function 做neural network。