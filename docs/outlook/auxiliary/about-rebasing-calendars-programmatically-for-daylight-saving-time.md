---
title: Сведения о программном переводе календарей на летнее время
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: В этом разделе этот период между весной и осенью называется периодом DST.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316957"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Сведения о программном переводе календарей на летнее время

Многие страны соблюдают летнее время (DST), продвигая часы, чтобы вечера были более длительными. Обычно это делается путем установки часов на час вперед весной и установки часов на час назад осенью. В этом разделе этот период между весной и осенью называется периодом DST. В большинстве стран имеются собственные правила для начала и окончания DST. Даты периода DST могут изменяться из года в год, и пользователи должны обновлять календарь Microsoft Outlook каждый раз, когда меняются правила DST. 
  
Если вы используете версию Windows, которая Windows Vista или более поздней версии, Windows автоматическое обновление включено, изменение DST может не затронуть вас. В противном случае необходимо установить обновления DST для Windows. Независимо от того, устанавливаются ли обновления автоматически, от вашего имени ИТ-отделом или самостоятельно в качестве домашнего пользователя, некоторые существующие встречи, которые происходят в период DST, могут отображаться неправильно после установки обновлений DST для Windows. Это относится как к повторяющимся, так и к единовременно встречам. Необходимо обновить эти встречи, чтобы правильно отображать их в Outlook, Outlook Web App и в приложениях, основанных на объектах данных совместной работы (CDO). Обновление неправильно отображаемой встречи в календарях из-за DST называется rebasing calendars.
  
Outlook предоставляет средства для пользователей, а Exchange Server предоставляет администраторам средства для повторной базы календарей. Outlook предоставляет средство обновления данных часовой зоны для Outlook пользователей. С помощью этого средства пользователи могут обновлять собственные календари. Exchange Server предоставляет средство обновления Exchange календаря, которое помогает администраторам избегать трудностей, которые возникают в результате широкой развертывания средства Outlook для всех пользователей, и убедиться, что каждый пользователь выполняет Outlook инструмент правильно.
  
Помимо того, что пользователи используют средство обновления данных часовой зоны или администраторы для запуска средства обновления календаря Exchange, сторонние разработчики клиентского программного обеспечения MAPI могут скачать DLL Tzmovelib.dll. С помощью этой сборки разработчики могут использовать те же API, которые Outlook и Exchange Server в средствах повторного использования календаря. 

В следующем списке показаны API для повторного сбоя в календаре:
  
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
    
Чтобы написать средство для повторного анализа встречи с помощью API для повторного использования календаря, можно использовать следующую процедуру:
  
1. Используйте **IOlkApptRebaser::BeginEnumerateAppointments** и **IOlkApptRebaser::EndEnumerateAppointments,** чтобы найти встречи, которые являются кандидатами на повторное использование. При необходимости предоставят сведения, позволяющие пользователю решать, какие встречи перебазжать. Кроме того, используйте MAPI или объектную модель Outlook, чтобы изучить сведения о времени и повторе при встрече, проанализировав свойства **PidLidAppointmentTimeZoneDefinitionStartDisplay,** **PidLidAppointmentTimeZoneDefinitionEndDisplay** и **Свойства PidLidAppointmentTimeZoneDefinitionRecur.** 
    
2. Чтобы перебазировать назначение, используйте **HrCreateApptRebaser,** **IOlkApptRebaseAppointments** и **IOlkApptRebaser::EndRebaseAppointments.** 
    
Чтобы получить сборку Tzmovelib.dll, скачайте перераспределяемый установщик OutlookTimeZoneMoveLibRedist.exe и файл загона Tzmovelib.h в [Outlook 2010 г.:](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)вспомогательный справочный перераспределяемый установщик и файл header для календарей повторного доступа. Эта загрузка работает Outlook 2010 и более поздних версиях Outlook. OutlookTimeZoneMoveLibRedist.exe устанавливается файл сборки Tzmovelib.dll C:\Program Files\MsExTmz. Обратите внимание, что сторонние приложения для повторного доступа к календарю могут перераспределять только установщик, OutlookTimeZoneMoveLibRedist.exe и не должны перераспределять сборку, Tzmovelib.dll или другие извлеченные компоненты отдельно от установщика.
  
## <a name="see-also"></a>См. также

- [Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Анализ потока из двоичного свойства для считывания структуры TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Анализ потока из двоичного свойства для считывания структуры TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Считывание свойств часового пояса встречи](how-to-read-time-zone-properties-from-an-appointment.md)
- [Центр помощи и поддержки по летнему времени](https://support.microsoft.com/gp/cp_dst)
- [Решение проблемы летнего времени с помощью средства обновления Exchange календаря](https://support.microsoft.com/kb/941018)
- [Устранение изменений часовых поясов с помощью средства обновления данных часовых поясов для Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

