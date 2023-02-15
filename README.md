# A-Single-Agent-Q-learning-Algorithm-for-2D-Maps

 
February 15, 2023![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.001.png)

The goal of this lab is to implement a Reinforcement algorithm -Q- Learning- to learn a policy that moves a robot to a goal position. The lab focus was to train the model to find the goal in a finite 2D environment that is closed and contains some obstacles. The robot will move one cell per iteration to the direction of the action that will be selected using a certain policy, unless there is an obstacle or the wall in front of it, in which case it will stay in the same position.

1. Learning Rate (α)

Figures [1 ](#_page0_x70.87_y319.81)and [2 ](#_page0_x70.87_y534.16)demonstrate the effect of having a very small and a very large α, respectively. A very small α results in a more stable convergence of reward whereas the reward progress of higher α is more sporadic, as expected.

1) Reward over Episodes![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.002.png)![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.003.png)
   2) Value Function

Figure 1: Effect of Small Learning Rate (α = 0.1)

1) Reward over Episodes![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.004.png)![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.005.png)
   2) Value Function

Figure 2: Effect of Large Learning Rate (α = 0.8)

2. Discount Factor (γ)

A factor of 0 will make the agent short-sighted as it will only consider the current action reward, while a factor of 1 will make it too biased for a long-term high reward. The visible difference between the graphs in Figure 3[ will](#_page1_x70.87_y211.20) be the stability of the reward value.

![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.006.png) ![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.007.png)

(a) Reward over Episodes (γ=0) (b) Reward over Episodes (γ=1)

Figure 3: Effect of Discount factor Rate (α = 0.5 , epsilon = 0.9)

1 Results

After tuning of parameters according to the factors discussed in the previous section, the results in Figure [4 ](#_page2_x70.87_y227.44)were obtained. The test shows that the agent is able to find path to the goal. Multiple variations in this map using different start and goal positions are tested and results are shown in ??.

![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.008.png) ![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.009.png)

(a) Value Function (b) optimal policy

![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.010.png)

(c) path

Figure 4: Original Map, Goal (3,18) : (α = 0.85 , epsilon = 0.9,γ = 0.9)

The algorithm was further tested in two different environments. As can be expected the parameters had to be tuned differently for them. The results are shown in Figures 5 [and](#_page3_x70.87_y245.55) ??.

` `![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.011.png)![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.012.png)

(a) Value Function (b) optimal policy

![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.013.png) ![](Aspose.Words.b062e3ec-fd14-400c-8e67-3fd50a13af7d.014.png)

(c) Map(2)- test(1) (d) Map(2)- test(2)

Figure 5: training Map(2), Goal (2,15) : (α = 0.9 , epsilon = 0.7,γ = 0.7)
4
