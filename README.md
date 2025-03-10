

On 21_05 

![image](https://github.com/user-attachments/assets/7295fc5d-1f95-4ee7-be40-b6f5b5fad40d)


![image](https://github.com/user-attachments/assets/b41f352b-f8ed-40ca-89d0-5e8c08778f36)


![image](https://github.com/user-attachments/assets/8101bbd7-e136-4614-89ae-c33b8604b3e2)

![image](https://github.com/user-attachments/assets/2f754bf0-779f-4b30-bba7-caee09f6b7f3)

![image](https://github.com/user-attachments/assets/bd08c2a4-9e2d-43e8-bb2f-9231ffec1ff5)


![image](https://github.com/user-attachments/assets/09a08e16-9cbc-4e3f-816a-1d1bd2da2c9d)







on 19_09 



![image](https://github.com/user-attachments/assets/72e02f3d-4066-4119-af34-9fa89cf8608c)
![image](https://github.com/user-attachments/assets/de582795-a986-468d-a2e6-33708971045b)
![image](https://github.com/user-attachments/assets/918d3805-e609-4f9d-a82e-b011e5731384)


![image](https://github.com/user-attachments/assets/abc5d135-0cbe-4a69-b946-7eabd2c3efad)



![image](https://github.com/user-attachments/assets/e4b3a386-b8dd-4c0a-8e96-da9daa72f6bc)



我来解释这个随机过程的收敛性问题，并重新详细说明这些步骤。

### 为什么 $Q_n$ 收敛

$Q_n = \prod_{i=1}^n (1 + Y_i)$ 收敛的原因是：

1. 由于 $Y_i \geq 0$（非负），所以 $Q_n$ 是单调递增的序列：$Q_0 = 1 \leq Q_1 \leq Q_2 \leq \ldots$

2. 给定条件 $\sum_i Y_i < \infty$ 几乎必然成立（a.s.），这意味着 $Y_i$ 的和是有限的。

3. 对于收敛性，我们可以利用对数变换：
   $\log(Q_n) = \log\left(\prod_{i=1}^n (1 + Y_i)\right) = \sum_{i=1}^n \log(1 + Y_i)$

4. 当 $Y_i$ 较小时，$\log(1 + Y_i) \approx Y_i$，更精确地说，对所有 $Y_i \geq 0$，我们有 $\log(1 + Y_i) \leq Y_i$

5. 因此 $\log(Q_n) = \sum_{i=1}^n \log(1 + Y_i) \leq \sum_{i=1}^n Y_i < \infty$ (a.s.)

6. 所以 $\log(Q_n)$ 收敛，这意味着 $Q_n$ 也收敛到某个有限值 $Q_{\infty} = \sup_n Q_n$

### 改进的证明步骤

让我重新详细阐述整个证明过程：

考虑适应过程 $Q_n = \prod_{i=1}^n (1 + Y_i) \geq Q_0 = 1$ 和 $W_n = (1 + X_n)/Q_{n-1}$。

**第一部分：$Q_n$ 的收敛性**

由于 $Y_i \geq 0$，$Q_n$ 是单调递增的。根据条件 $\sum_i Y_i < \infty$ (a.s.)，我们可以证明 $Q_n$ 收敛：

对于任意 $Y_i \geq 0$，我们有不等式 $\log(1+Y_i) \leq Y_i$，因此：
$\log(Q_n) = \sum_{i=1}^n \log(1+Y_i) \leq \sum_{i=1}^n Y_i < \infty$ (a.s.)

这表明 $\log(Q_n)$ 有上界，因此 $Q_n$ 收敛到某个有限极限 $Q_{\infty} = \sup_n Q_n < \infty$ (a.s.)。

**第二部分：$W_n$ 是超鞅**

我们来验证 $W_n$ 是超鞅。计算条件期望：

$\mathbf{E}(W_{n+1}|\mathcal{F}_n) = \mathbf{E}\left(\frac{1 + X_{n+1}}{Q_n}|\mathcal{F}_n\right)$

由于 $Q_n$ 是 $\mathcal{F}_n$ 可测的，我们可以将其提出条件期望：

$\mathbf{E}(W_{n+1}|\mathcal{F}_n) = \frac{1}{Q_n}\mathbf{E}(1 + X_{n+1}|\mathcal{F}_n)$

根据给定的关系，我们有：
$\mathbf{E}(1 + X_{n+1}|\mathcal{F}_n) \leq (1 + Y_n)(1 + X_n)$

因此：
$\mathbf{E}(W_{n+1}|\mathcal{F}_n) \leq \frac{(1 + Y_n)(1 + X_n)}{Q_n} = \frac{(1 + Y_n)(1 + X_n)}{Q_{n-1}(1+Y_n)} = \frac{1 + X_n}{Q_{n-1}} = W_n$

这证明了 $W_n$ 是超鞅。

**第三部分：$W_n$ 和 $X_n$ 的收敛性**

由于 $X_n \geq 0$，所以 $W_n = \frac{1 + X_n}{Q_{n-1}} \geq \frac{1}{Q_{n-1}} > 0$，即 $W_n$ 是非负的。

根据 Doob 超鞅收敛定理，非负超鞅 $W_n$ 几乎必然收敛到某个有限极限 $W_{\infty}$。

最后，由于 $X_n = W_n Q_{n-1} - 1$，且 $Q_{n-1}$ 和 $W_n$ 都收敛到有限极限，因此 $X_n$ 也收敛到有限极限 $X_{\infty} = W_{\infty}Q_{\infty} - 1$ (a.s.)。


