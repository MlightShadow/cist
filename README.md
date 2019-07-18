# continued image-style-transfor

参考

[neural-style](https://github.com/anishathalye/neural-style)

[image-style-transfor](https://github.com/harry19902002/image-style-transfor)

## 快速开始

因为已经更新到使用最新的依赖, 直接安装我给出的`requirements.txt`即可

```bash
git clone https://github.com/MlightShadow/cist.git

cd cist

wget http://www.vlfeat.org/matconvnet/models/imagenet-vgg-verydeep-19.mat

pip install -r requirements.txt

python neural_style.py --content content.jpg --styles style.jpg --output output.jpg
```

## 已经做的改动

`scipy.misc` 中的 `imread()`与`imsave()` 方法已经在1.2版本被相继废除, 查阅资料后我们这边使用 `imageio` 来替代 `scipy.misc`

* `imageio.imread()` -> `scipy.misc.imread()`
* `imageio.imsave()` -> `scipy.misc.imwrite()`

另外 `scipy.misc.resize()` 也被废除了, 这边用`skimage`来替代, 不过`skimage`也需要使用`scikit-image`来替代了 `scikit-image` 包括 `imageio`
