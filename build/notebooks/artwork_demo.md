
This is an example notebook. It does not require any external data resources, and so can be run during continuous integration checks.


```python
%run setup.ipynb
```


<style type="text/css">
.container {
    width: 100%;
}
#maintoolbar {
    display: none;
}
#header-container {
    display: none;
}
div#notebook {
    padding-top: 0;
}
</style>



```python
x = np.arange(100)
x
```




    array([ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16,
           17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33,
           34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50,
           51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67,
           68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84,
           85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99])




```python
y = np.linspace(0, 1, 100)
y
```




    array([ 0.        ,  0.01010101,  0.02020202,  0.03030303,  0.04040404,
            0.05050505,  0.06060606,  0.07070707,  0.08080808,  0.09090909,
            0.1010101 ,  0.11111111,  0.12121212,  0.13131313,  0.14141414,
            0.15151515,  0.16161616,  0.17171717,  0.18181818,  0.19191919,
            0.2020202 ,  0.21212121,  0.22222222,  0.23232323,  0.24242424,
            0.25252525,  0.26262626,  0.27272727,  0.28282828,  0.29292929,
            0.3030303 ,  0.31313131,  0.32323232,  0.33333333,  0.34343434,
            0.35353535,  0.36363636,  0.37373737,  0.38383838,  0.39393939,
            0.4040404 ,  0.41414141,  0.42424242,  0.43434343,  0.44444444,
            0.45454545,  0.46464646,  0.47474747,  0.48484848,  0.49494949,
            0.50505051,  0.51515152,  0.52525253,  0.53535354,  0.54545455,
            0.55555556,  0.56565657,  0.57575758,  0.58585859,  0.5959596 ,
            0.60606061,  0.61616162,  0.62626263,  0.63636364,  0.64646465,
            0.65656566,  0.66666667,  0.67676768,  0.68686869,  0.6969697 ,
            0.70707071,  0.71717172,  0.72727273,  0.73737374,  0.74747475,
            0.75757576,  0.76767677,  0.77777778,  0.78787879,  0.7979798 ,
            0.80808081,  0.81818182,  0.82828283,  0.83838384,  0.84848485,
            0.85858586,  0.86868687,  0.87878788,  0.88888889,  0.8989899 ,
            0.90909091,  0.91919192,  0.92929293,  0.93939394,  0.94949495,
            0.95959596,  0.96969697,  0.97979798,  0.98989899,  1.        ])




```python
z = x * y
z
```




    array([  0.00000000e+00,   1.01010101e-02,   4.04040404e-02,
             9.09090909e-02,   1.61616162e-01,   2.52525253e-01,
             3.63636364e-01,   4.94949495e-01,   6.46464646e-01,
             8.18181818e-01,   1.01010101e+00,   1.22222222e+00,
             1.45454545e+00,   1.70707071e+00,   1.97979798e+00,
             2.27272727e+00,   2.58585859e+00,   2.91919192e+00,
             3.27272727e+00,   3.64646465e+00,   4.04040404e+00,
             4.45454545e+00,   4.88888889e+00,   5.34343434e+00,
             5.81818182e+00,   6.31313131e+00,   6.82828283e+00,
             7.36363636e+00,   7.91919192e+00,   8.49494949e+00,
             9.09090909e+00,   9.70707071e+00,   1.03434343e+01,
             1.10000000e+01,   1.16767677e+01,   1.23737374e+01,
             1.30909091e+01,   1.38282828e+01,   1.45858586e+01,
             1.53636364e+01,   1.61616162e+01,   1.69797980e+01,
             1.78181818e+01,   1.86767677e+01,   1.95555556e+01,
             2.04545455e+01,   2.13737374e+01,   2.23131313e+01,
             2.32727273e+01,   2.42525253e+01,   2.52525253e+01,
             2.62727273e+01,   2.73131313e+01,   2.83737374e+01,
             2.94545455e+01,   3.05555556e+01,   3.16767677e+01,
             3.28181818e+01,   3.39797980e+01,   3.51616162e+01,
             3.63636364e+01,   3.75858586e+01,   3.88282828e+01,
             4.00909091e+01,   4.13737374e+01,   4.26767677e+01,
             4.40000000e+01,   4.53434343e+01,   4.67070707e+01,
             4.80909091e+01,   4.94949495e+01,   5.09191919e+01,
             5.23636364e+01,   5.38282828e+01,   5.53131313e+01,
             5.68181818e+01,   5.83434343e+01,   5.98888889e+01,
             6.14545455e+01,   6.30404040e+01,   6.46464646e+01,
             6.62727273e+01,   6.79191919e+01,   6.95858586e+01,
             7.12727273e+01,   7.29797980e+01,   7.47070707e+01,
             7.64545455e+01,   7.82222222e+01,   8.00101010e+01,
             8.18181818e+01,   8.36464646e+01,   8.54949495e+01,
             8.73636364e+01,   8.92525253e+01,   9.11616162e+01,
             9.30909091e+01,   9.50404040e+01,   9.70101010e+01,
             9.90000000e+01])




```python
# assume 8 inches width available for figures that go in the manuscript
plt.figure(figsize=(8, 5))
plt.plot(x, z);
plt.savefig('../artwork/demo.png', bbox_inches='tight', dpi=300);
```


![png](artwork_demo_files/artwork_demo_5_0.png)



```python
plt.figure()
plt.plot(x, z, 'k.');
```


![png](artwork_demo_files/artwork_demo_6_0.png)



```python

```