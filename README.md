# Rabbi Ovadiah Yosef Zmanim Website and Apps

<p align="center">
	<img src="https://is1-ssl.mzstatic.com/image/thumb/Purple211/v4/cc/4f/de/cc4fded5-598f-1f3a-eaa6-26405d119a93/AppIcon-0-0-1x_U007epad-0-11-0-85-220.png/217x0w.webp" width="200px" alt="logo">
</p>

This repository is the main hub that links to all of the projects that help you find zemanim according to Rabbi Ovadiah Yosef ZT"L: the Android app (with Wear OS), the iOS app (with watchOS and widgets), and the official website.

<table align="center">
  <tr>
    <td align="center" width="33%"><strong>Google Play Store</strong></td>
    <td align="center" width="33%"><strong>App Store</strong></td>
    <td align="center" width="33%"><strong>Website</strong></td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <a href="https://play.google.com/store/apps/details?id=com.EJ.ROvadiahYosefCalendar&amp;pcampaignid=pcampaignidMKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1">
        <img alt="Get it on Google Play" src="https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png" width="200px">
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://apps.apple.com/app/rabbi-ovadiah-yosef-calendar/id6448838987">
        <img alt="Get it on the App Store" src="https://ci6.googleusercontent.com/proxy/HrtBTHlFE3VpRkzLfRwnYbJjCLtCpmKOIV__qk9k9mj7e7PSZF2X0L7mzR63nCIfqbnUujbn-dhiq-LwYUqdcpSLg_ItRhdEQJ0wP438309hcA=s0-d-e1-ft#https://static.licdn.com/aero-v1/sc/h/76yzkd0h5kiv27lrd4yaenylk" width="200px">
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://royzmanim.com/">
        <img src="https://cdn-icons-png.flaticon.com/512/5602/5602732.png" width="100px" alt="Website">
      </a>
    </td>
  </tr>

  <tr>
    <td align="center" width="33%"><strong>Android Source Code</strong></td>
    <td align="center" width="33%"><strong>iOS Source Code</strong></td>
    <td align="center" width="33%"><strong>Website Source Code</strong></td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <a href="https://github.com/Zemaneh-Yosef/RabbiOvadiahYosefCalendarAndroidApp">
        <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" width="50px" alt="GitHub">
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://github.com/Zemaneh-Yosef/RabbiOvadiahYosefCalendarIOSApp">
        <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" width="50px" alt="GitHub">
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://github.com/Zemaneh-Yosef/royzmanimwebsite">
        <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" width="50px" alt="GitHub">
      </a>
    </td>
  </tr>
</table>

# Goal of the project:
The original goal of this project was to recreate the "Luach HaMaor Ohr HaChaim" calendar that is widespread in Israel. This calendar is special because Rabbi Ovadiah Yosef ZT"L oversaw its creation and used the calendar himself until he passed. It is considered to be the most accurate calendar for people who want to follow Rabbi Ovadia Yosef's practices:

<p align="center">
<img src="https://i.imgur.com/QqGAtTB.jpg" height="750" alt="Picture of Ohr HaChaim calendar">
</p>

In order to recreate the calendar, we needed an API that would give the times for sunrise and sunset every day (since all the other zemanim (times) are based on sunrise/sunset). I was recommended the well known [KosherJava](https://github.com/KosherJava/zmanim) package for its accuracy and transparency, and that is the basis for all of the apps' calculations:

- **Android / Wear OS:** [KosherJava](https://github.com/KosherJava/zmanim)
- **iOS / watchOS:** [KosherSwift](https://github.com/Elyahu41/KosherSwift), my Swift port of KosherJava. (The iOS app originally used KosherCocoa, but it was not as fleshed out as KosherJava.)
- **Website:** [KosherZmanim](https://github.com/BehindTheMath/KosherZmanim), the TypeScript port of KosherJava.

The apps were originally made primarily for English speakers, however, they have been localized for both English and Hebrew speakers.

The only zeman that could not be computed by the KosherJava API is the sunrise time that the Ohr HaChaim calendar uses. They explain in the calendar introduction that they take the sunrise times from a calendar called "Luach Bechoray Yosef". That calendar calculates the time for sunrise by taking into account the geography of the land around that area (which is around 40GB of data) and finding when is the first time the sun is seen in that area (based on the introduction to Chaitables.com). While not impossible, this would take a massive toll on a mobile phone's processor, memory, and storage space, therefore, the apps do not support these sunrise calculations natively. However, I discovered that the creator of this calendar made a website, [ChaiTables.com](http://chaitables.com), to help people use his algorithm for sunrise/sunset all over the world and create a 12 month table based on your input. I added the ability to download these times in the apps with your own specific parameters. (It is highly recommended that you see the introduction on chaitables.com before setting the advanced parameters.)

After the Ohr HaChaim calendar was implemented and fully functional, we implemented Rabbi Leeor Dahan's calendar (Amudei Horaah) for areas outside of Israel. The Ohr HaChaim calendar was made for Israel and it needed a few adjustments to be applicable outside of Israel. We confirmed this with both of Rabbi Ovadia Yosef's sons (Rabbi Yitzhak Yosef and Rabbi David Yosef).

Rabbi Meir Gavriel Elbaz and Rabbi Leeor Dahan themselves have given [haskamot](https://royzmanim.com/) for this project, and with their help we were able to even receive a [haskama](https://royzmanim.com/assets/haskamah-rishon-letzion.pdf) from Rabbi Yitzhak Yosef.

# Android App Screenshots:
| <img src="https://play-lh.googleusercontent.com/zVHLQfLFEFi042B5fs8aospA9rEHQYI9lhEpBDl5WJtO7DXpWf5KHOyJwGcJt6FL6g"> | <img src="https://play-lh.googleusercontent.com/qqzs-vMfkBYOb7MhE8GSSDrgxnT3SHPnvOUVZ5-hpmPKNRmGDlKk_ZfWgFPRjoyS9Zk"> | <img src="https://play-lh.googleusercontent.com/M2rFetNy9kZJoVpi6EV0w07TagYgV7pdCaSH-d46p_tjjaydrbrjCA-8ytfBJ57BSzI"> | <img src="https://play-lh.googleusercontent.com/M5ngIENjzFAu3Jr_6uPMPR7ZL5axZa7wXjXj-l3T2UR1NwWHnDhgK5cwymG92_dH9g"> |
| ---------------------------------------------- | -------------------------------------------- | ------------------------------------------ | ------------------------------------------- |

| <img src="https://play-lh.googleusercontent.com/x9-dPIKcVofd0Bzd1Pncp7YTKItC9dPtP0ZU8swd3Q-ee2ySTkyiscXTssF_eNPfgnk"> | <img src="https://play-lh.googleusercontent.com/4_ieNYmeCYv75lGsuOg95fT5-1v7vK8zuvSbOV78MtMWWKLS-PIDS2dTT9MCTz4vX4FP"> | <img src="https://play-lh.googleusercontent.com/ZiT9dliscrbOqqwxdpzivXE77Hpt-CMpgUcT-8x1MVnDPZp6jVOTpdes5Dgg9l4Okg"> | <img src="https://play-lh.googleusercontent.com/goFEBByE3neELxuURq_G7LtO_QkuQCs8WPnu5Ltx57Elx62k5FgCWqWDuIfobqagMs2u"> |
| ---------------------------------------------- | -------------------------------------------- | ------------------------------------------ | ------------------------------------------- |

# Wear OS Screenshots:
| <img src="https://play-lh.googleusercontent.com/vMzSm9w5hfmr4ObCemKkU99tePQqzgtBFGPU_Iz5AxbWwHJUcd9lxP7AGvnYiVlaLuyGKJapYzSB-66GUlQZlw=w526-h296-rw"> | <img src="https://play-lh.googleusercontent.com/2foqoiwrJHKCZm0Kl_ENFjkiTgeyVIzB56EhkBn1SQWBBsW-_J1g-TkzWbR-AtZuNXGifOscQbqaRZcIDBAAaDg=w526-h296-rw"> | <img src="https://play-lh.googleusercontent.com/IhrLgqYireND5Cfu8JRu-b-t_JlQCEMrCf6Xswc_k6RtT2qvt_AQrGoZp1SJe-SawD-7Vnzvar-_CQT6EVKmG_c=w526-h296-rw"> | <img src="https://play-lh.googleusercontent.com/yYKAwh3jAW7W6xGv34-s20p3J6SLuLk223yqb7AIAx6qo2wN3zBwWW00OHqqJQboQkTaG06zn9tmVYvKLdIr2n8=w526-h296-rw"> |
| ---------------------------------------------- | -------------------------------------------- | ------------------------------------------ | ------------------------------------------- |

| <img src="https://play-lh.googleusercontent.com/nFK8Uaw4TeQt3ICxnCt0LDN52GtVSo9mJmtY3_uL_JRFq2PmrFlDDmyD_iITMzu0mwOPIxEmDdQoviH44c_QwOY=w526-h296-rw"> | <img src="https://play-lh.googleusercontent.com/rTXIe0loU0v6-Fb3J7HJnN4keRrgYIyAGfJB-YEo316AW0osgKASi6xCQifENnQPSneHK7gsPemLPgWf3Uzg=w526-h296-rw"> | <img src="https://play-lh.googleusercontent.com/vLcROLwyviwIaOoGbAH2rQpBBOls--UBhwctCI1QoEMIPH_0hROE6RZCVQwE1vPJoXtpBl7l-SqPkziQOU2HN90=w526-h296-rw"> | <img src="https://play-lh.googleusercontent.com/UHEI5egChtT5Zqe_-Wgg-5xCQz-4D4ieoSPeX4L0Ja90Y2HuUm5M1tFE36UgcjEIgGt2Dl05W5_cBdlAWchb=w526-h296-rw"> |
| ---------------------------------------------- | -------------------------------------------- | ------------------------------------------ | ------------------------------------------- |

# iOS App Screenshots:
| <img src="https://is1-ssl.mzstatic.com/image/thumb/PurpleSource211/v4/75/f7/24/75f72459-c2d9-b0e0-4ef4-202a3c2594d2/Simulator_Screenshot_-_iPhone_16_Pro_-_2025-05-27_at_16.53.24.png/230x0w.webp"> | <img src="https://is1-ssl.mzstatic.com/image/thumb/PurpleSource211/v4/dd/06/e3/dd06e3e5-06bd-4937-a157-83013e9e3483/Simulator_Screenshot_-_iPhone_16_Pro_-_2025-05-25_at_03.26.28.png/230x0w.webp"> | <img src="https://is1-ssl.mzstatic.com/image/thumb/PurpleSource221/v4/8f/c5/e6/8fc5e6e6-cc98-1896-adf0-0e18c7e44716/Simulator_Screenshot_-_iPhone_16_Pro_-_2025-05-25_at_03.28.06.png/230x0w.webp"> | <img src="https://is1-ssl.mzstatic.com/image/thumb/PurpleSource221/v4/5c/ce/7c/5cce7c64-3281-a635-6136-c84814c9e6bd/Simulator_Screenshot_-_iPhone_16_Pro_-_2025-05-25_at_03.28.49.png/230x0w.webp"> |
| ---------------------------------------------- | -------------------------------------------- | ------------------------------------------ | ------------------------------------------- |

| <img src="https://is1-ssl.mzstatic.com/image/thumb/PurpleSource221/v4/cc/1d/b7/cc1db7e1-d73a-f049-b13e-ea72e1cac2e3/Simulator_Screenshot_-_iPhone_16_Pro_-_2025-05-25_at_03.29.48.png/230x0w.webp"> | <img src="https://is1-ssl.mzstatic.com/image/thumb/PurpleSource221/v4/3f/92/84/3f9284fb-d69a-81cb-25fd-c9ef80c28225/Simulator_Screenshot_-_iPhone_16_Pro_-_2025-05-25_at_03.30.54.png/230x0w.webp"> | <img src="https://is1-ssl.mzstatic.com/image/thumb/PurpleSource221/v4/ab/74/39/ab7439db-2a35-e5dc-946c-2f69b3025331/Simulator_Screenshot_-_iPhone_16_Pro_-_2025-05-25_at_03.31.55.png/230x0w.webp"> | <img src="https://is1-ssl.mzstatic.com/image/thumb/PurpleSource211/v4/8d/aa/62/8daa62a8-15cf-0e85-b922-2f5f780386bf/Simulator_Screenshot_-_iPhone_16_Pro_-_2025-05-25_at_03.32.44.png/230x0w.webp"> |
| ---------------------------------------------- | -------------------------------------------- | ------------------------------------------ | ------------------------------------------- |

# Explanation of how the zemanim are calculated:
- For an in-depth explanation of each specific time, please look at the descriptions for each individual time, found in the apps themselves.
- For an explanation of the differences between outside of Israel and inside of Israel, or whether or not to use elevation, please visit our [FAQ](https://royzmanim.com/FAQ).
- An overview of the Ohr HaChaim calculations is below. Outside of Israel, the Amudei Horaah calendar adjusts Alot HaShachar and Tzeit based on the degrees of the sun (see [Amudei Horaah](#amudei-horaah-calendar-outside-of-israel) below).

<details>
<summary><b>Overview of each zeman (Ohr HaChaim calendar)</b></summary>

<br>

**Dawn - Alot HaShachar:**
This time is calculated as 72 zmaniyot/seasonal minutes (according to the GR"A) before sunrise. Both sunrise and sunset have elevation included.

**Misheyakir - Earliest Talit/Tefilin:**
This time is calculated as 6 zmaniyot/seasonal minutes (according to the GR"A) after Alot HaShachar (Dawn).

**Sunrise - HaNetz:**
As explained above, the Luach Bechoray Yosef calculates the time for sunrise based on the surrounding geography. If the user does not download the times from ChaiTables, the apps default to Mishor/Sea Level Sunrise provided by the KosherJava API.

**Eating Chametz - Achilat Chametz:**
This is calculated as 4 zmaniyot/seasonal hours, according to the Magen Avraham, after Alot HaShachar (Dawn) with elevation included.

**Burning Chametz - Biur Chametz:**
This is calculated as 5 zmaniyot/seasonal hours, according to the MG"A, after Alot HaShachar (Dawn) with elevation included.

**Latest time for Shma (MG"A):**
The Magen Avraham/Terumat HeDeshen calculates this time as 3 zmaniyot/seasonal hours after Alot HaShachar (Dawn). They calculate a zmaniyot/seasonal hour by taking the time between Alot HaShachar (Dawn) and Tzeit Hachocavim (Nightfall) of Rabbeinu Tam and dividing it into 12 equal parts.

**Latest time for Shma (GR"A):**
The GR"A calculates this time as 3 zmaniyot/seasonal hours after sunrise (elevation included). The GR"A calculates a zmaniyot/seasonal hour by taking the time between sunrise and sunset (elevation included) and dividing it into 12 equal parts.

**Brachot Shma:**
The GR"A calculates this time as 4 zmaniyot/seasonal hours after sunrise (elevation included).

**Mid-Day - Chatzot:**
This time is calculated as 6 zmaniyot/seasonal hours after sunrise.

**Earliest Mincha - Mincha Gedolah:**
This time is calculated as 30 regular minutes after Chatzot (Mid-Day). However, if the zmaniyot/seasonal minutes are longer, we use those minutes instead to be stringent.

**Mincha Ketana:**
This time is calculated as 9 and a half zmaniyot/seasonal hours after sunrise.

**Plag HaMincha:**
This time is usually calculated as 10 and 3/4 zmaniyot/seasonal hours after sunrise, however, Yalkut Yosef writes to calculate it as 1 hour and 15 zmaniyot/seasonal minutes before Tzeit.

**Candle Lighting:**
This time is calculated as 20 regular minutes before sunset (elevation included) by default. You can change this in the settings.

**Sunset - Shkia:**
Halachic sunset is defined as the moment when the top edge of the sun disappears on the horizon while setting (elevation included).

**Nightfall - Tzeit Hacochavim:**
This time is calculated as 13 and a half zmaniyot/seasonal minutes after sunset (elevation included). NOTE: This time is very early in the winter, especially in the far north or south. This zeman should NOT be used to decide when Shabbat ends or any other serious matters without consulting a rabbi first!

**Fast Ends - Tzeit Taanit:**
This time is displayed twice: the first time is calculated as 20 regular minutes after sunset (elevation included) and the second time is calculated as 30 minutes after sunset.

**Shabbat/Chag Ends - Tzeit Shabbat/Chag:**
There are many customs on when Shabbat ends. By default, it is set to 40 regular minutes after sunset (elevation included), however, you can change the time in the settings.

**Rabbeinu Tam:**
This time is calculated as 72 zmaniyot/seasonal minutes after sunset (elevation included). Another way of calculating this time is by calculating how many minutes are between sunrise and sunset, dividing that number by 10, and adding the result to sunset.

**Midnight - Chatzot Layla:**
This time is calculated as 6 zmaniyot/seasonal hours after sunset. In this case, we use sunrise of the next day.

<i>Note: Unless stated otherwise, a zmaniyot/seasonal hour (GR"A) is the time between sunrise and sunset (elevation included) divided into 12 equal parts, and a zmaniyot/seasonal minute is one of those parts divided by 60.</i>

</details>

# Amudei Horaah calendar (outside of Israel)
Rabbi Leeor Dahan Shlita, author of the "Amudei Horaah" on the Mishna Berurah, has created his own "Amudei Horaah" calendar. It is similar to the Ohr HaChaim calendar, except the zemanim for Alot and Tzeit are adjusted based on the degrees of the sun. To explain: if normally Alot is 72 zmaniyot minutes before sunrise, Rabbi Dahan holds that we need to find out how many minutes are between Alot and sunrise on an equal day (equinox). To do this, we use degrees based on Netanya, Israel (since the gemara equates Iraq and Israel as the same area). Once you have that amount of minutes, you make them zmaniyot based on sunrise to sunset. For example, Alot in New York is around 81 zmaniyot minutes before sunrise. He bases these calculations on the Halacha Berurah (Siman 261, halacha 13).

With the Rabbi's help, his zemanim have been added to all of the apps and the website, and they are used for locations outside of Israel. You can also change which calendar is used in the settings.

# Introduction and haskama to the calendar in Israel:

| <img src="https://royzmanim.com/assets/images/sources/OHhaskama.png" height="250" alt="haskama"> | <img src="https://royzmanim.com/assets/images/sources/intro1.png" height="250" alt="intro 1"> | <img src="https://royzmanim.com/assets/images/sources/intro2.png" height="250" alt="intro 2"> | <img src="https://royzmanim.com/assets/images/sources/intro3.png" height="250" alt="intro 3"> |
| ---------------------------------------------- | -------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
