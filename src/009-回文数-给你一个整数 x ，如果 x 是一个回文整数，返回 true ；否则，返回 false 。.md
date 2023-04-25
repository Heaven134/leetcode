问题描述

    给你一个整数 x ，如果 x 是一个回文整数，返回 true ；否则，返回 false 。
    回文数是指正序（从左向右）和倒序（从右向左）读都是一样的整数。

思路

    两个指针分别指向首、尾元素，判断所指元素是否相等，然后指针分别向后移与向前移。现在的问题在于，题目给的参数为int型，如果要实现上述操作，那操作对象就需要是数组或字符串形式。我们这里选取字符串来进行操作
    将int转换为String类型方法：


代码(java)

    public static boolean isPalindrome(int x) {
            String str = String.valueOf(x);
            //String s = Integer.toString(x);
            int n = str.length();
            for (int i = 0, j = n - 1; i < str.length() / 2; i++, j--) {
                if(str.charAt(i) != str.charAt(j)){
                    return false;
                }
            }
            return true;
        }

