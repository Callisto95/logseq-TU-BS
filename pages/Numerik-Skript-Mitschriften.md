- 16
  collapsed:: true
	- $$y_0=0\Rightarrow y\left(t\right)=\frac{t^2}{1+t^2}$$
	- $$y_0=-\varepsilon\Rightarrow\tilde{y}\left(t\right)=-\varepsilon e^{10t}+\frac{t^2}{1+t^2}$$
- 19
  collapsed:: true
	- $$\Phi\left(t_{i},u_{i},h_{i}\right)=f\left(t_{i},u_{i}\right)$$
- 21
  collapsed:: true
	- $$\tau\left(t,h\right)=\frac{y\left(t+h\right)-y\left(t\right)}{h}-f\left(t,y\left(y\right)\right)=\frac{y\left(t\right)+hy^{\prime}\left(t\right)+O\left(h^2\right)-y\left(t\right)}{h}=O\left(h\right)$$
	- 2.8: Ableitung mit Kettenregel
- 23
  collapsed:: true
	- $$\Rightarrow\left|y_{i+1}-u_{i+1}\right|=\left|\left\lbrack y_{i}+h\left(Ly_{i}+\tau\left(t_{i},h\right)\right)\right\rbrack-\left\lbrack u_{i}+hLu_{i}\right\rbrack\right|\leq\left(1+hL\right)\left|y_{i}-u_{i}\right|+Ch^2$$
	- $$\Rightarrow\left|y_1-u_1\right|\leq\left(1+hL\right)\left|y_0-u_0\right|+Ch^2$$
	- $$\left|y_2-u_2\right|\leq\left(1+hL\right)\left|y_1-u_1\right|+Ch^2$$
	- $$\leq\left(1+hL\right)\left\lbrack\left(1+hL\right)\left|y_0-u_0\right|+Ch^2\right\rbrack+Ch^2$$
	- $$\leq\left(1+hL\right)^2\left(\left|y_0-u_0\right|+2Ch^2\right)$$
	- $$\Rightarrow\left|y_{N}-u_{N}\right|\leq\left(1+hL\right)^{N}\left(\left|y_0-u_0\right|+NCh^2\right)$$
		- dabei
			- $$\left(1+hL\right)^{N}\rightarrow e^{L}$$
			- $$NCh^2\rightarrow Ch$$
- 26
  collapsed:: true
	- 2.11
		- $$\dot{y}=3y\equiv f\left(t,y\right)\Rightarrow\left|f\left(t,y_1\right)-f\left(t,y_2\right)\right|=3\left|y_1-y_2\right|\Rightarrow L=3$$
	- 2.12
		- $$\dot{y}=10\left(y-\frac{t^2}{1+t^2}\right)+\frac{2t}{\left(1+t^2\right)^2}\equiv f\left(t,y\right)\Rightarrow\left|f\left(t,y_1\right)-f\left(t,y_2\right)\right|=10\left|y_1-y_2\right|\Rightarrow L=10$$
- 27
  collapsed:: true
	- 2.13
		- $$c,m,d>0,A=\begin{pmatrix}0 & 1\\ -\frac{c}{m} & -\frac{d}{m}\end{pmatrix}\Rightarrow\left|\left|A\right|\right|_{\infty}=\max\left\lbrace a,\frac{c}{m}+\frac{d}{m}\right\rbrace,\left|\left|A\right|\right|_1=\max\left\lbrace\frac{c}{m},1+\frac{d}{m}\right\rbrace$$
- 28
  collapsed:: true
	- 2.14
		- $$m\dot{\dot{x}}+d\dot{x}+cx+mg=0$$
		- $$\text{mit }v=\dot{x}$$
		- $$\Rightarrow\left\lbrace_{\dot{v}=-\frac{d}{m}v-\frac{c}{m}x-g}^{\dot{x}=v}\right.\Rightarrow\begin{pmatrix}\dot{x}\\ \dot{v}\end{pmatrix}=\begin{pmatrix}0 & 1\\ -\frac{c}{m} & -\frac{d}{m}\end{pmatrix}\begin{pmatrix}x\\ v\end{pmatrix}+\begin{pmatrix}0\\ -g\end{pmatrix}\equiv\overrightarrow{f}\left(t,\overrightarrow{y}\right)$$
		- $$\left|\left|\overrightarrow{f}\left(t,\overrightarrow{y}_2\right)-\overrightarrow{f}\left(t,\overrightarrow{y}_2\right)\right|\right|_{\infty}=\left|\left|A\left(\overrightarrow{y}_1-\overrightarrow{y}_2\right)\right|\right|_{\infty}\leq\left|\left|A\right|\right|_{\infty}\left|\left|\overrightarrow{y}_1-\overrightarrow{y}_2\right|\right|_{\infty}$$
		- $$\left|\left|A\right|\right|_{\infty}=\max\left\lbrace1,\frac{c}{m}+\frac{d}{m}\right\rbrace\equiv L$$
- 32
  collapsed:: true
	- 3.1
		- $$r=1\cdot2^4+0\cdot2^3+0\cdot2^2+1\cdot2^1+0\cdot2^0+1\cdot2^{-1}=\left(10010.1\right)_2$$
		- $$r=1\cdot16^2+2\cdot16^1+8\cdot16^0=\left(12.8\right)_{16}$$
- 34
  collapsed:: true
	- 3.2
		- $$r_1=-0.123456789\cdot10^4\hat{=}-123456789+4$$
		- $$r_2=-0.123456789\cdot10^{-1}\hat{=}-123456789-1$$
- 44,45,46
  collapsed:: true
	- nope :)
- 87
  collapsed:: true
	- $$=\frac{\left|\varepsilon\right|\left|x_1+x_2\right|}{\left|x_1+x_2\right|}\leq\epsilon\frac{\left|x_1\right|+\left|x_2\right|}{\left|x_1+x_2\right|}$$
- 88
  collapsed:: true
	- $$=F\left(\tilde{x}_1,\tilde{x}_2\right)$$
	- $$=\frac{\left|\varepsilon\right|\left|\left|\begin{pmatrix}x_1\\ x_2\end{pmatrix}\right|\right|}{???}$$
- 91
  collapsed:: true
	- $$1-\sqrt{1-\sigma}=\frac{1^2-\sqrt{1-\sigma}^2}{1+\sqrt{1-\sigma}}=\frac{\sigma}{1+\sqrt{1-\sigma}}$$
- 105
	- $$a_0-2a_1+4a_2-8a_3=10$$
	- $$a_0-a_1+a_2-a_3=4$$
	- $$a_0+a_1+a_2+a_3=6$$
	- $$a_0+2a_1+4a_2+8a_3=3$$
	-
- ---
- 1
  collapsed:: true
	- $$\dot{y}=f\left(t,y\right)$$
	- $$y\left(t_0\right)$$
	- $$\frac{y\left(t+h\right)-y\left(t\right)}{h}-\Phi\left(t,y,h\right)=O\left(h^{p}\right)$$
	- $$h<<1\text{ konsistent von der Ordnung p}$$
	- $$M_0=y_0,...$$
	- $$M_{i+1}=M_{i}+h_{i}\Phi\left(t_{i},M_{i},h_{i}\right)\text{ mit }i=0,1,2,...$$
	- $$M_{i}\approx y\left(t_{i}\right)$$
	- $$\left|M_{i}-y\left(t_{i}\right)\right|\leq Ch^{p}\cdot O\left(h^{p}\right)\text{ Konvergenz der Ordnung p}$$
- 2
  collapsed:: true
	- $$m\dot{\dot{x}}+d\dot{x}+cx+f=0$$
	- $$v=\dot{x}$$
	- $$\begin{pmatrix}\dot{x}\\ \dot{v}\end{pmatrix}=\begin{pmatrix}v\\ -\frac{d}{m}v-\frac{c}{m}x-\frac{f}{m}\end{pmatrix}=\begin{pmatrix}0 & 1\\ -\frac{c}{m} & -\frac{d}{m}\end{pmatrix}\begin{pmatrix}x\\ v\end{pmatrix}+\begin{pmatrix}0\\ -\frac{f}{m}\end{pmatrix}$$
	-
- implizites Euler Verfahren
  collapsed:: true
	- $$y\left(t+h\right)=y\left(t\right)+h\cdot f\left(t+h,y\left(t+h\right)\right)$$
	- $$g\left(y\left(t+h\right)\right)=g\left(t+h\right)-g\left(t\right)-h\cdot f\left(t+h,y\left(t+h\right)\right)=0$$
	- $$g\left(y\right)=0$$
	- $$\dot{y}=L\cdot y,y\left(0\right)=1,y=e^{l\cdot t}$$
	- $$u\left(t+h\right)=u\left(t\right)+h\cdot L\cdot u\left(t+h\right)\Leftrightarrow\left(1-h\cdot L\right)\cdot u\left(t+h\right)=u\left(t\right)$$
	- $$\Leftrightarrow u\left(t+h\right)=\frac{u\left(t\right)}{1-h\cdot L}\Leftrightarrow u\left(k\cdot h\right)=\frac{1}{\left(1-k\cdot h\right)^{k}}$$
	- $$L=-1000,h=\frac{1}{100}\Rightarrow\frac{1}{\left(1+9\right)^{k}}$$
-