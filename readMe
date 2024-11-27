pager class
```


class PagerTransformer(
    private val viewPager2: ViewPager2,
    private val onChangePosition: (position: Float) -> Unit
) : ViewPager2.PageTransformer {

    private var swipeToLeft = true
    private var swipeToRight = true

    override fun transformPage(page: View, position: Float) {
        onChangePosition(position)

        if (viewPager2.currentItem == (viewPager2.adapter?.itemCount ?: 0) - 2 && swipeToLeft) { // son sayfa giriş
            if (position < 0) {
                page.translationX = -position * page.width
            } else {
                page.translationX = position
            }
        }
        else if (viewPager2.currentItem == (viewPager2.adapter?.itemCount ?: 0) - 1 && swipeToRight) { // son sayfa çıkış
            if (position < 0) {
                page.translationX = -position * page.width
            } else {
                page.translationX = position
            }
        }
        else {
            page.translationX = position
        }


    }
}

```



