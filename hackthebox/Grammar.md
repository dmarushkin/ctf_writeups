# Grammar web challenge write-up

We've got 403 error:
![](https://i.imgur.com/nQZuYFA.png)

After some struggling found that POST to index.php works:

![](https://i.imgur.com/wkxt3Ht.png)

![](https://i.imgur.com/MvhcKyu.png)

We have cookie in base64:

![](https://i.imgur.com/OpEUkbt.png)

Changing Admin:False to True didn't work, but with setting mac to 0 we;ve got good result

![](https://i.imgur.com/NXRB3u7.png)

Flag:

![](https://i.imgur.com/j9Lu0vV.png)
