# -LV4-
柳永华的LV4作业
《《时间戳的转换》》

import java.text.SimpleDateFormat;
import java.util.Date;
public class DateFormatUtil{
private String Date;
        public String getDate () {
        return Date;
    }
        public void setDate (String date){
        Date = date;
    }
    public static void main(String[] args){
        Long timeStamp = System.currentTimeMillis();
        SimpleDateFormat sdf=new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        String sd = sdf.format(new Date(Long.parseLong(String.valueOf(timeStamp))));
        System.out.println("" + sd);
        SimpleDateFormat sdf2 = new SimpleDateFormat("yyyy 年 MM 月 dd 日 HH 时 mm 分 ss 秒");
        String sd2 = sdf2.format(new Date(Long.parseLong(String.valueOf(timeStamp))));
        System.out.println("" + sd2);
    }
}

《《时间的转换》》

import java.util.Date;
import java.text.SimpleDateFormat;
public class DateFormatUtil {
private String Date;
        public String getDate () {
        return Date;
    }
        public void setDate (String date){
        Date = date;
    }
    public static void main(String[] args) {
        SimpleDateFormat sdf = new SimpleDateFormat();
        sdf.applyPattern("yyyy-MM-dd HH:mm:ss a");
        Date date = new Date();
        System.out.println("现在时间：" + sdf.format(date));
        Long  timeStamp =System.currentTimeMillis();
        SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy 年 MM 月 dd 日 HH 时 mm 分 ss 秒");
                System.out.println("" +sdf1.format(timeStamp));
    }
}

《《时间差的计算》》

import java.util.Date;
import java.text.SimpleDateFormat;
public class DateFormatUtil {
    public static void main(String[] args) {
        SimpleDateFormat sdf = new SimpleDateFormat();
        try {
            Date d1 = sdf.parse("你输入的第一个时间");
            Date d2 = sdf.parse("你输入的第二个时间");
            long diff = d1.getTime() - d2.getTime();
            long days = diff / (1000 * 60 * 60 * 24);
            long hours = (diff - days * (1000 * 60 * 60 * 24)) / (1000 * 60 * 60);
            long minutes = (diff - days * (1000 * 60 * 60 * 24) - hours * (1000 * 60 * 60)) / (1000 * 60);
            System.out.println("" + days + "天" + hours + "小时" + minutes + "分");
        } catch (Exception e) {
        }
    }
}
