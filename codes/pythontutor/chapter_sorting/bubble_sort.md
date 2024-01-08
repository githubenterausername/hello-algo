<!--
    File: bubble_sort.md
    Created Time: 2024-01-05
    Author: Krahets (krahets@163.com)
--->

<!-- [file]{bubble_sort}-[class]{}-[func]{bubble_sort} -->
https://pythontutor.com/render.html#code=def%20bubble_sort%28nums%3A%20list%5Bint%5D%29%3A%0A%20%20%20%20%22%22%22%E5%86%92%E6%B3%A1%E6%8E%92%E5%BA%8F%22%22%22%0A%20%20%20%20n%20%3D%20len%28nums%29%0A%20%20%20%20%23%20%E5%A4%96%E5%BE%AA%E7%8E%AF%EF%BC%9A%E6%9C%AA%E6%8E%92%E5%BA%8F%E5%8C%BA%E9%97%B4%E4%B8%BA%20%5B0,%20i%5D%0A%20%20%20%20for%20i%20in%20range%28n%20-%201,%200,%20-1%29%3A%0A%20%20%20%20%20%20%20%20%23%20%E5%86%85%E5%BE%AA%E7%8E%AF%EF%BC%9A%E5%B0%86%E6%9C%AA%E6%8E%92%E5%BA%8F%E5%8C%BA%E9%97%B4%20%5B0,%20i%5D%20%E4%B8%AD%E7%9A%84%E6%9C%80%E5%A4%A7%E5%85%83%E7%B4%A0%E4%BA%A4%E6%8D%A2%E8%87%B3%E8%AF%A5%E5%8C%BA%E9%97%B4%E7%9A%84%E6%9C%80%E5%8F%B3%E7%AB%AF%0A%20%20%20%20%20%20%20%20for%20j%20in%20range%28i%29%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20if%20nums%5Bj%5D%20%3E%20nums%5Bj%20%2B%201%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%23%20%E4%BA%A4%E6%8D%A2%20nums%5Bj%5D%20%E4%B8%8E%20nums%5Bj%20%2B%201%5D%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20nums%5Bj%5D,%20nums%5Bj%20%2B%201%5D%20%3D%20nums%5Bj%20%2B%201%5D,%20nums%5Bj%5D%0A%0A%22%22%22Driver%20Code%22%22%22%0Aif%20__name__%20%3D%3D%20%22__main__%22%3A%0A%20%20%20%20nums%20%3D%20%5B4,%201,%203,%201,%205,%202%5D%0A%20%20%20%20bubble_sort%28nums%29%0A%20%20%20%20print%28%22%E5%86%92%E6%B3%A1%E6%8E%92%E5%BA%8F%E5%AE%8C%E6%88%90%E5%90%8E%20nums%20%3D%22,%20nums%29&cumulative=false&curInstr=4&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=311&rawInputLstJSON=%5B%5D&textReferences=false

<!-- [file]{bubble_sort}-[class]{}-[func]{bubble_sort_with_flag} -->
https://pythontutor.com/render.html#code=def%20bubble_sort_with_flag%28nums%3A%20list%5Bint%5D%29%3A%0A%20%20%20%20%22%22%22%E5%86%92%E6%B3%A1%E6%8E%92%E5%BA%8F%EF%BC%88%E6%A0%87%E5%BF%97%E4%BC%98%E5%8C%96%EF%BC%89%22%22%22%0A%20%20%20%20n%20%3D%20len%28nums%29%0A%20%20%20%20%23%20%E5%A4%96%E5%BE%AA%E7%8E%AF%EF%BC%9A%E6%9C%AA%E6%8E%92%E5%BA%8F%E5%8C%BA%E9%97%B4%E4%B8%BA%20%5B0,%20i%5D%0A%20%20%20%20for%20i%20in%20range%28n%20-%201,%200,%20-1%29%3A%0A%20%20%20%20%20%20%20%20flag%20%3D%20False%20%20%23%20%E5%88%9D%E5%A7%8B%E5%8C%96%E6%A0%87%E5%BF%97%E4%BD%8D%0A%20%20%20%20%20%20%20%20%23%20%E5%86%85%E5%BE%AA%E7%8E%AF%EF%BC%9A%E5%B0%86%E6%9C%AA%E6%8E%92%E5%BA%8F%E5%8C%BA%E9%97%B4%20%5B0,%20i%5D%20%E4%B8%AD%E7%9A%84%E6%9C%80%E5%A4%A7%E5%85%83%E7%B4%A0%E4%BA%A4%E6%8D%A2%E8%87%B3%E8%AF%A5%E5%8C%BA%E9%97%B4%E7%9A%84%E6%9C%80%E5%8F%B3%E7%AB%AF%0A%20%20%20%20%20%20%20%20for%20j%20in%20range%28i%29%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20if%20nums%5Bj%5D%20%3E%20nums%5Bj%20%2B%201%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%23%20%E4%BA%A4%E6%8D%A2%20nums%5Bj%5D%20%E4%B8%8E%20nums%5Bj%20%2B%201%5D%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20nums%5Bj%5D,%20nums%5Bj%20%2B%201%5D%20%3D%20nums%5Bj%20%2B%201%5D,%20nums%5Bj%5D%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20flag%20%3D%20True%20%20%23%20%E8%AE%B0%E5%BD%95%E4%BA%A4%E6%8D%A2%E5%85%83%E7%B4%A0%0A%20%20%20%20%20%20%20%20if%20not%20flag%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20break%20%20%23%20%E6%AD%A4%E8%BD%AE%E2%80%9C%E5%86%92%E6%B3%A1%E2%80%9D%E6%9C%AA%E4%BA%A4%E6%8D%A2%E4%BB%BB%E4%BD%95%E5%85%83%E7%B4%A0%EF%BC%8C%E7%9B%B4%E6%8E%A5%E8%B7%B3%E5%87%BA%0A%0A%22%22%22Driver%20Code%22%22%22%0Aif%20__name__%20%3D%3D%20%22__main__%22%3A%0A%20%20%20%20nums%20%3D%20%5B4,%201,%203,%201,%205,%202%5D%0A%20%20%20%20bubble_sort_with_flag%28nums%29%0A%20%20%20%20print%28%22%E5%86%92%E6%B3%A1%E6%8E%92%E5%BA%8F%E5%AE%8C%E6%88%90%E5%90%8E%20nums%20%3D%22,%20nums%29&cumulative=false&curInstr=4&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=311&rawInputLstJSON=%5B%5D&textReferences=false