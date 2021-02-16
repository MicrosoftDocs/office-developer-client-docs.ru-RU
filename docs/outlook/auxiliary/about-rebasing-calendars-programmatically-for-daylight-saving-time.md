---
title: Сведения о программном переводе календарей на летнее время
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: В этом разделе этот период между пружиной и осенней периодами называется периодом DST.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316957"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Сведения о программном переводе календарей на летнее время

Во многих странах летнее время (DST) соблюдается за счет настроив часы таким образом, чтобы в дневное время было больше летнего времени. Как правило, это делается путем настройки часов на час вперед в пружиной среде и установки часов на час назад в осеннюю. В этом разделе этот период между пружиной и осенней периодами называется периодом DST. В большинстве стран имеются собственные правила для начала и окончания DST. Даты периода летнего времени могут меняться из года в год, и пользователи должны обновлять календарь Microsoft Outlook каждый раз, когда меняются правила DST. 
  
Если вы используете версию Windows Vista или более поздней версии или включили автоматическое обновление Windows, изменение DST может не повлиять на вас. В противном случае следует установить обновления DST для Windows. Независимо от того, устанавливаются ли обновления автоматически, от вашего имени ИТ-отделом или самим пользователем дома, некоторые существующие встречи, которые происходят в период DST, могут отображаться неправильно после установки обновлений DST для Windows. Это справедливо как для повторяющихся встреч, так и для встреч с одним экземпляром. Эти встречи необходимо обновить, чтобы они правильно отображались в Outlook, Outlook Web App и в приложениях, основанных на объектах данных совместной работы (CDO). Неправильно отображаемая встреча в календарях из-за DST называется переустанавливка календарей.
  
Outlook предоставляет средства для пользователей и Exchange Server предоставляет администраторам средства для перебазки календарей. Outlook предоставляет средство обновления данных часовой пояс для пользователей Outlook. С помощью этого средства пользователи могут обновлять собственные календари. Exchange Server предоставляет средство обновления календаря Exchange, которое помогает администраторам избежать проблем, которые возникают при развертывании средства Outlook для всех пользователей, и убедиться, что каждый пользователь правильно запускает средство Outlook.
  
Помимо того, что пользователи могут запускать средство обновления данных часового пояса или администраторы для запуска средства обновления календаря Exchange, сторонние разработчики клиентского программного обеспечения MAPI могут скачать DLL,Tzmovelib.dll. С помощью этой сборки разработчики могут использовать те же API, что и Outlook Exchange Server в своих средствах повторного применения календаря. 

В следующем списке показаны API для повторного сбоя календаря:
  
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
    
Чтобы написать средство повторного применения встреч с помощью API-api для повторного применения календаря, можно использовать следующую процедуру:
  
1. Используйте **IOlkApptRebaser::BeginEnumerateAppointments** и **IOlkApptRebaser::EndEnumerateAppointments,** чтобы найти встречи, которые являются кандидатами для повторного применения. При необходимости предо представить сведения, позволяющие пользователю решить, какие встречи необходимо перебазжать. Кроме того, используйте MAPI или объектную модель Outlook, чтобы изучить сведения о времени и повторе встречи, проанализировав свойства **PidLidAppointmentTimeZoneDefinitionStartDisplay,** **PidLidAppointmentTimeZoneDefinitionEndDisplay** и **PidLidAppointmentTimeZoneDefinitionRecur.** 
    
2. Используйте **HrCreateApptRebaser,** **IOlkApptRebaser::BeginRebaseAppointments** и **IOlkApptRebaser::EndRebaseAppointments** для перебазации встречи. 
    
Чтобы получить сборку Tzmovelib.dll, скачайте распространяемый установщик OutlookTimeZoneMoveLibRedist.exe и файл заглавных файлов Tzmovelib.h в [Outlook 2010: вспомогательный](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)распространяемый установщик ссылок и файл загона для повторного разрешения календарей. Эта загрузка работает для Outlook 2010 и более поздних версий Outlook. OutlookTimeZoneMoveLibRedist.exe установит Tzmovelib.dll сборки в папке C:\Program Files\MsExTmz. Обратите внимание, что сторонние приложения для повторного применения календаря могут распространять только установщик, OutlookTimeZoneMoveLibRedist.exe и не должны распространять сборку, Tzmovelib.dll или любые другие извлеченные компоненты отдельно от установщика.
  
## <a name="see-also"></a>См. также

- [Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Анализ потока из двоичного свойства для считывания структуры TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Анализ потока из двоичного свойства для считывания структуры TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Считывание свойств часового пояса встречи](how-to-read-time-zone-properties-from-an-appointment.md)
- [Центр справки и поддержки для перехода на летнее время](https://support.microsoft.com/gp/cp_dst)
- [Как решить проблему перехода на летнее время с помощью средства обновления календаря Exchange](https://support.microsoft.com/kb/941018)
- [Устранение изменений часовых поясов с помощью средства обновления данных часовых поясов для Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

