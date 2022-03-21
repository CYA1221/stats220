# Assignment1

## Here's my meme made using the R package [{magick}](https://cran.r-project.org/web/packages/magick/vignettes/intro.html).

![](my_meme.png)

The new thing in the meme is:

1. ELDEN RING is a game that just released
2. ELDEN RING is the continuation of the DARK SOULS
3. It's really fun and i just played it  XD

#the code is here
"drake_1 <- image_read("https://pyxis.nymag.com/v1/imgs/62c/fa8/6e52acce958795508a7ecbf6a3656c0190-11-drake-hotline-bling.rsquare.w700.jpg") %>%
  image_scale(500)

dark_souls_text <- image_blank(width = 500, 
                          height = 500, 
                          color = "#000000") %>%
  image_annotate(text = "DARK\nSOULs",
                 color = "#FFFFFF",
                 size = 80,
                 font = "Impact",
                 gravity = "center")

drake_2 <- image_read("https://i.imgur.com/PwxHfBb.png") %>%
  image_scale(500)

elden_ring_text <- image_blank(width = 500, 
                               height = 500, 
                               color = "#000000") %>%
  image_annotate(text = "ELDEN\nRING",
                 color = "#FFFFFF",
                 size = 80,
                 font = "Impact",
                 gravity = "center")
top_row <- c(drake_1, dark_souls_text)%>%
    image_append
bot_row <- c(drake_2, elden_ring_text)%>%
    image_append
meme <- c(top_row, bot_row) %>%
  image_append(stack = TRUE) %>%
  image_scale(800)
image_write(meme, "my_meme.png")"
