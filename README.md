<img width="435" alt="image" src="https://github.com/user-attachments/assets/965290ac-31c4-41b7-b859-a299e9351973" />


On 21_05 

![image](https://github.com/user-attachments/assets/7295fc5d-1f95-4ee7-be40-b6f5b5fad40d)


![image](https://github.com/user-attachments/assets/b41f352b-f8ed-40ca-89d0-5e8c08778f36)


on 19_09 

![image](https://github.com/user-attachments/assets/74d98ff8-a398-4a65-b39c-5c8a49fe20e6)


![image](https://github.com/user-attachments/assets/fe30ac96-9ef9-4ae2-bea2-c437395d99d2)



Here’s a more formal, math-heavy version suitable for a PowerPoint slide:  

---

### **Markov Decision Process (MDP)**  
*Foundation of Q-Learning*  

An MDP is defined by the tuple **\( M = (S, A, P, r, \gamma) \)**, where:  

- **\( S \)**: A finite set of states.  
- **\( A \)**: A finite set of actions.  
- **\( P: S \times A \to \Delta(S) \)**: A probability transition function, where  
  \[
  P(s' \mid s, a) = \Pr(S_{t+1} = s' \mid S_t = s, A_t = a)
  \]  
  represents the probability of transitioning to state \( s' \) given state \( s \) and action \( a \).  
- **\( r: S \times A \to [0,1] \)**: A reward function that defines the immediate reward \( r(s, a) \) for taking action \( a \) in state \( s \).  
- **\( \gamma \in (0,1) \)**: A discount factor that determines the present value of future rewards, ensuring convergence of the value function.  



This version keeps the formal mathematical notation while maintaining clarity for a PowerPoint slide. Let me know if you need modifications!
