# ⚡ Optimizer Behaviour – Learning Rate Issues (MLE-A Exam)

## 🚩 Symptoms of Too High Learning Rate
- Training + validation loss stay high.  
- Loss **oscillates** (drops, then spikes up, repeating).  

## ✅ Correct Fix
- **Reduce the learning rate** → smaller gradient steps, smoother convergence, prevents oscillation.  

## ❌ Wrong Options
- **Increase epochs** → only prolongs oscillation, no fix.  
- **Increase learning rate** → makes oscillation worse.  
- **Apply dropout** → helps generalization/overfitting, not convergence stability.  

## ⚡ Exam Hack
- **Oscillating loss** = learning rate too high → **reduce LR**.  
- **Loss decreasing too slowly** = learning rate too low → **increase LR**.  

👉 Memory rule: **Bouncing loss → lower LR; Crawling loss → raise LR.**
