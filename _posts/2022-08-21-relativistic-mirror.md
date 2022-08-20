---
layout: post
title: "Relativistic Mirror"
author: "Zinc"
tags: first markdown example
categories: gallery
---

 <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
      }
    });
  </script>
  <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  TeX: { equationNumbers: { autoNumber: "AMS" } }
});
</script>

## **Relativistic Mirror**


### **Problem**

An observer who is fixed to the frame of reference $K$, observing a perfect reflecting mirror moving with the speed $v = \beta c$, where $c$ is the speed of light in vacuum. The velocity vector of the mirror passes the observer's eyes so that he/she can see his/her image through the mirror. There is a marker on the mirror so that the observer can easily determine where the mirror in space is.

**a,** Find the apparent and real velocity of the image and the mirror.

**b,** If the light consists of photons with wavelength $\lambda_0$, what will the wavelength $\lambda$ of photons that the observer capture be?


### **Solution**

Xét một tia sáng đi đến gương với góc tới $\alpha$ và phản xạ lại với góc $\beta$. Trong hệ quy chiếu mà gương đứng yên, tia sáng sẽ đi tới với góc $\theta$ và phản xạ lại với góc $\theta' = \theta$.

\vspace{1mm}

Sử dụng các công thức cộng vận tốc tương đối tính ta có các phương trình:
$$c'_x = c \cos \theta = c \cdot\frac{\cos \alpha - \frac{v}{c}}{1 - \frac{v}{c} \cos \alpha}.$$
$$c"_x = c \cos \beta = \frac{c'_x - v}{1 - \frac{v}{c^2} c'_x} = c \cdot \frac{\cos \alpha - 2\frac{v}{c} + \frac{v^2}{c^2 \cos \alpha}}{1 - 2\frac{v}{c} \cos \alpha + \frac{v^2}{c^2}}.$$

Theo công thức chia đôi góc lượng giác ta có:
$$\tan \frac{\beta}{2} = \sqrt{\frac{1 - \cos \beta}{1 + \cos \beta}} = \sqrt{\frac{(1 - \cos \alpha)\left(1 + \frac{v}{c} \right)^2}{(1 + \cos \alpha)\left(1 - \frac{v}{c} \right)^2}}.$$

$$\Rightarrow \tan \frac{\beta}{2} =  \frac{c + v}{c - v} \cdot \tan \frac{\alpha}{2} = 3 \tan \frac{\alpha}{2}.$$

Do cách đặt mắt chính diện nên $\alpha, \beta \approx 0$, do đó $\beta \approx 3 \alpha$. 

Từ đó ta suy ra được vận tốc của ảnh:
$$v' = \frac{d}{dt} (x + x') = v \left(\frac{\alpha}{\beta} + 1 \right) = \frac{2v}{1 + \frac{v}{c}} =\frac{2}{3} c. \hspace{0.5em} \text{\textit{(Sai!)}}$$

Quan điểm về vận tốc của ảnh ở phương trình trên là chưa chính xác, bởi vì ta đã ngộ nhận rằng ánh sáng phát từ nguồn sáng S và tới mắt ngay lập tức (trong trường hợp cổ điển).

\vspace{1mm}

Xét hai xung ánh sáng liên tiếp phát ra có chu kì $\Delta \tau$ từ nguồn sáng S. Khoảng cách ban đầu giữa gương và S là $d$, đặt mốc thời gian $t = 0$ là lúc tia sáng thứ nhất phát ra. Sau khi tia sáng thứ nhất phát ra và đập vào gương thì lúc đó toạ độ tia sáng là:
$$x_1 = \frac{c}{c-v} d, \quad t_1 = \frac{d}{c- v}.$$
Toạ độ tia sáng thứ hai lúc nó đập vào gương là:
$$x_2 = \frac{c}{c-v} (d + v \Delta \tau), \quad t_2 = \Delta \tau + \frac{d+ v\Delta \tau}{c - v}.$$

Lúc tia sáng về mắt người, mắt người sẽ nhận được thông tin về toạ độ của ảnh S' là:
$$x'_1 = \frac{2}{1 + \frac{v}{c}} x_1, \quad t'_1 = 2t_1.$$
$$x'_2 = \frac{2}{1 + \frac{v}{c}} x_2, \quad t'_2 = 2t_2 - \Delta \tau.$$
Từ đó ta suy ra được vận tốc biểu kiến của ảnh là:
$$v' = \frac{\Delta x'}{\Delta t'} = \frac{2v}{\left(1 + \frac{v}{c} \right)^2} = \frac{4}{9} c.$$


Nhận thấy rằng kết quả vừa tính sai khác với kết quả ngộ nhận một hệ số $\frac{1}{1+ \frac{v}{c}}$. Khi $v \ll c$ thì có thể coi như sự truyền sáng là ngay lập tức.
