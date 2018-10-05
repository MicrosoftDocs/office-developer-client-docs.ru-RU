---
title: Сведения о программном переводе календарей на летнее время
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: В этом разделе этот период между пружин и попадающих называется период летнего времени.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389024"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Сведения о программном переводе календарей на летнее время

Во многих странах выполняли летнего времени (переход на летнее время) путем перемещения часы, так что вечером больше времени перехода на летнее. Обычно это делается путем установки часы час издержек в пружин, а также установка часы час предлагаем. В этом разделе этот период между пружин и попадающих называется период летнего времени. Большинство стран имеют собственные правила перехода на летнее время начинается и заканчивается. Дат периода летнего времени можно изменить по годам и пользователи должны обновить их календаря Microsoft Outlook каждый раз, что изменение правилам летнего времени. 
  
При использовании версии Windows, Windows Vista или более поздней версии, или операционная система, включить автоматическое обновление, которое не подвержена влиянию переход на летнее время. В противном случае следует установить обновления летнего времени для Windows. Независимо от того, является ли обновления будут установлены автоматически, от вашего имени у ИТ-подразделения, или у себя как дома некоторые существующие встреч, которые происходят в период летнего времени могут отображаться неправильные время после установки обновлений летнего времени для Windows . Это характерно для повторяющихся и единичных встреч. Необходимо обновить эти встречи для правильного отображения их в Outlook, Outlook Web App и приложения, основанные на объекты данных совместной работы (CDO). Обновление неправильно отображаемым встреч в календарях из-за перехода на летнее время называется повторного размещения календарей.
  
Outlook предоставляет средства для пользователей и Exchange Server предоставляет средства для администраторов rebase календарей. Outlook предоставляет средство обновления данных часового пояса для пользователей Outlook. С помощью этого средства пользователи могут обновлять свои собственные календари. Exchange Server предоставляет средства обновления календаря Exchange, помогающих администраторам во избежание проблем, которые возникают из широко развертывания средства Outlook для всех пользователей и убедитесь в том, что каждый пользователь запускает средство Outlook правильно.
  
В дополнение к полагаться на пользователям запускать средство обновления данных часового пояса или администраторами для запуска средства обновления календаря Exchange, клиентского программного обеспечения сторонних производителей MAPI разработчики могут загрузить библиотеки DLL Tzmovelib.dll. С помощью этой сборки, разработчики могут использовать одинаковые интерфейсы API, Outlook и Exchange Server в их повторного размещения en средства календаря. 

В следующем списке приведены календаря, повторного размещения en API-интерфейсов:
  
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
    
Для записи средство сдвига встречи в календаре, повторного размещения en API-интерфейсы, можно использовать следующую процедуру:
  
1. Чтобы найти встречи, которые подходят для повторного размещения en используйте **IOlkApptRebaser::BeginEnumerateAppointments** и **IOlkApptRebaser::EndEnumerateAppointments** . В случае необходимости представить сведения, которые пользователь может решить, какие встреч в rebase. Кроме того используйте MAPI или объектной модели Outlook для проверки сведений о времени и повторения встречи синтаксический анализ **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay** и **PidLidAppointmentTimeZoneDefinitionRecur** свойства. 
    
2. Используйте **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments**и **IOlkApptRebaser::EndRebaseAppointments** для перебазирование встречи. 
    
Для получения Tzmovelib.dll сборки, загрузите распространяемый установщик OutlookTimeZoneMoveLibRedist.exe и файл заголовка Tzmovelib.h в [Outlook 2010: дополнительный распространяемого установщика ссылки и файл заголовка для повторного размещения en календарей](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b) . Этот загружаемый файл работает для Outlook 2010 и более поздних версий Outlook. OutlookTimeZoneMoveLibRedist.exe устанавливает файл сборки Tzmovelib.dll в C:\Program Files\MsExTmz. Обратите внимание, что сдвига приложениями сторонних производителей календаря можно распространять только установщика, но OutlookTimeZoneMoveLibRedist.exe и не должен распространять сборки, Tzmovelib.dll или любой другой извлекать компоненты отдельно от установщика.
  
## <a name="see-also"></a>См. также

- [About persisting TZDEFINITION to a stream to commit to a binary property](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Анализ потока из двоичного свойства для считывания структуры TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Анализ потока из двоичного свойства для считывания структуры TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Считывание свойств часового пояса встречи](how-to-read-time-zone-properties-from-an-appointment.md)
- [Летнее время Справка и поддержка](https://support.microsoft.com/gp/cp_dst)
- [Как летнее время с помощью средства обновления календаря Exchange](https://support.microsoft.com/kb/941018)
- [Способы устранения изменения часового пояса, используя средство обновления данных часового пояса для Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

