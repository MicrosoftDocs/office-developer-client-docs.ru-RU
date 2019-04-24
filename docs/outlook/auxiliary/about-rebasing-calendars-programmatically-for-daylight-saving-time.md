---
title: Сведения о программном переводе календарей на летнее время
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: В этом разделе этот период между пружиной и находящимися точками называется периодом летнего времени.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316957"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Сведения о программном переводе календарей на летнее время

Во многих странах летнее время (DST) заменяется на летнее время, чтобы у вечера было больше времени на летнее время. Обычно это делается путем установки часов в течение часа в пружину и установки часов в качестве часа в отпадает. В этом разделе этот период между пружиной и находящимися точками называется периодом летнего времени. У большинства стран есть свои нормативы по началу и концу летнего времени. Даты периода летнего времени могут изменяться в течение года, а пользователи должны обновлять свой календарь Microsoft Outlook каждый раз, когда меняется нормативный период летнего времени. 
  
Если вы используете версию Windows, которая используется в Windows Vista или более поздней версии, или включили автоматическое обновление Windows, вы не можете изменить значение летнего времени. В противном случае следует установить обновления летнего времени для Windows. Независимо от того, установлены ли обновления автоматически, от вашего имени отдела ИТ или от вашего домашнего пользователя, некоторые из существующих встреч, произошедших в течение периода летнего времени, могут отображаться неправильно после установки обновлений для Windows на ЛЕТНее время. . Это относится и к повторяющимся встречам, и к одному экземпляру. Необходимо обновить эти встречи, чтобы правильно отобразить их в Outlook, в Outlook Web App и в приложениях, основанных на объектах данных совместной работы (CDO). Обновление неправильно отображенных встреч в календарях из-за DST называется изменением базового календаря.
  
Outlook предоставляет средства для пользователей и Exchange Server, которые позволяют администраторам перебазовых календарей. Outlook предоставляет средство обновления данных о часовых поясах для пользователей Outlook. С помощью этого средства пользователи могут обновлять собственные календари. Exchange Server предоставляет средство обновления календаря Exchange, помогающее администраторам избежать проблем, которые могут возникнуть при развертывании средства Outlook для всех пользователей, а также для проверки того, что каждый пользователь правильно работает с средством Outlook.
  
Помимо того, что пользователи могут запускать средство обновления данных о часовых поясах или администраторов для запуска средства обновления календаря Exchange, сторонние клиентские разработчики программного обеспечения для MAPI могут скачать БИБЛИОТЕКУ DLL, Тзмовелиб. dll. С помощью этой сборки разработчики могут использовать одни и те же API, которые Outlook и Exchange Server используют в своих средствах для базового календаря. 

В следующем списке показаны API, которые переводятся на основе календаря:
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Чтобы написать инструмент для базового отсчета встреч с помощью API на основе базового календаря, можно использовать следующую процедуру:
  
1. Используйте **иолкапптребасер:: бегиненумератеаппоинтментс** и **Иолкапптребасер:: енденумератеаппоинтментс** , чтобы найти встречи, которые являются кандидатами для перебазового. Если необходимо, представьте себе сведения, чтобы позволить пользователю решить, какие встречи необходимо перестроить. Кроме того, можно использовать MAPI или объектную модель Outlook, чтобы проверить время и сведения о повторении встречи путем синтаксического анализа **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay** и свойства **PidLidAppointmentTimeZoneDefinitionRecur** . 
    
2. Используйте **хркреатеапптребасер**, **Иолкапптребасер:: бегинребасеаппоинтментс**и **иолкапптребасер:: ендребасеаппоинтментс** , чтобы перестроить встречу. 
    
Чтобы получить сборку Тзмовелиб. dll, скачайте установщик распространяемого пакета Аутлуктимезонемовелибредист. exe и файл заголовков Тзмовелиб. h в [Outlook 2010: вспомогательНый справочНый файл программы установки и заголовочНый файл для перебазового календаря.](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b) . Этот загружаемый файл работает для Outlook 2010 и более поздних версий Outlook. Аутлуктимезонемовелибредист. exe устанавливает файл сборки Тзмовелиб. dll в папке C:\Program Филес\мсекстмз. Обратите внимание на то, что сторонние приложения календаря могут распространять только установщик, Аутлуктимезонемовелибредист. exe и не должны повторно распространять сборку, Тзмовелиб. dll или любые другие извлеченные компоненты отдельно от установщика.
  
## <a name="see-also"></a>См. также

- [Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Анализ потока из двоичного свойства для считывания структуры TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Анализ потока из двоичного свойства для считывания структуры TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Считывание свойств часового пояса встречи](how-to-read-time-zone-properties-from-an-appointment.md)
- [Центр справки и поддержки для летнего времени](https://support.microsoft.com/gp/cp_dst)
- [Как устранить летнее время с помощью средства обновления календаря Exchange](https://support.microsoft.com/kb/941018)
- [Устранение изменений часового пояса с помощью средства обновления данных о часовых поясах для Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

