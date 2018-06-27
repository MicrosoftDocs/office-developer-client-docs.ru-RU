---
title: Об API сведениям о доступности
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: Свободен/занят API позволяет поставщиков почты для предоставления сведений о доступности состояния для заданным учетным записям пользователей в рамках в заданном диапазоне времени.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807677"
---
# <a name="about-the-freebusy-api"></a>Об API сведениям о доступности

Свободен/занят API позволяет поставщиков почты для предоставления сведений о доступности состояния для заданным учетным записям пользователей в рамках в заданном диапазоне времени. Состояние занятости интервал времени в календаре пользователя — одно из следующих значений: документов office, «занят», под вопросом или бесплатное.
  
## <a name="create-a-freebusy-provider"></a>Создание поставщика сведений о доступности

Для предоставления сведений о доступности для пользователей почты, поставщик почты создает поставщика сведений о доступности и регистрирует его с помощью Outlook. Поставщик занятости должен реализовывать следующие интерфейсы. Обратите внимание, что число элементов в этих интерфейсов, не поддерживается и должен возвращать указанного возвращаемого значения. В частности о доступности API не поддерживает доступ на запись к сведения о доступности и передача прав доступа к учетным записям.
  
- [IFreeBusySupport](ifreebusysupport.md) — этот интерфейс поддерживает спецификации интерфейсов, доступ к сведениям о доступности данных для указанных пользователей. [FBUser](fbuser.md) используется для идентификации пользователя. 
    
- [IFreeBusyData](ifreebusydata.md) — этот интерфейс возвращает и задает диапазон времени для определенного пользователя и возвращает интерфейс для перечисления сведений о доступности блоков данных в пределах этого диапазона времени. Относительное время используется для получения и задания этот диапазон времени. Дополнительные сведения можно [Использовать относительное время для доступа к сведениям о доступности данных](how-to-use-relative-time-to-access-free-busy-data.md).
    
- [IEnumFBBlock](ienumfbblock.md) — этот интерфейс поддерживает доступ к и перечисление занятости блоков данных для пользователя в интервал времени. 
    
   > [!NOTE]
   > Перечисление содержит блоки сведениям о доступности, которые указывают состояние занятости периодов времени в календаре пользователя, в интервал времени (указывается с [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)). Элементы в календаре, например, встреч и приглашений на собрания, формирующие блоки в перечислении. Элементы, которые располагаются вплотную друг с другом в календаре и с таким же статусом занятости объединяются форме одну один блок. Бесплатная период времени в календаре также форм блока. Таким образом не два последовательных блоков в перечислении будет иметь же состояние сведений о доступности. Эти блоки не перекрывались времени. Если есть перекрывающиеся элементы календаря, Outlook объединяет эти элементы для без перекрытия блоков сведений о доступности в перечисление, основанное на этом приоритет: документов office, «занят», под вопросом. 
  
Чтобы зарегистрировать поставщик сведениям о доступности с помощью Outlook, поставщик почты должен выполните следующее:
  
1. Зарегистрируйте поставщика занятости COM, предоставляя CLSID, который позволяет получить доступ к реализации поставщика **IFreeBusySupport**. 
    
2. Программа Outlook знать, что поставщик занятости существует, установив следующий раздел (где `<xx.x>` представляет версию Outlook) в системном реестре: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Например если поставщика транспорта SMTP, чтобы зарегистрировать поставщик с помощью Microsoft Outlook 2010 установите следующий раздел к данным в следующей таблице: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Имя |Тип |Значение |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID для соответствующих реализации IFreeBusySupport}  |
   
   В этом сценарии Outlook совместно создает класс COM и используется для получения сведений о доступности для всех пользователей почты SMTP.
    
Чтобы обеспечить поддержку адресной книги и транспорта поставщик, использовать запись адреса, отличного от SMTP, соответствующим образом измените *имя* . 
  
> [!NOTE]
> Во время установки, занятости поставщиков должен проверить, будет ли параметров реестра для того же типа записи адресов уже существует. Если это так, поставщика сведениям о доступности следует перезапись текущего поставщика для этого типа адреса запись и восстановление этому поставщику во время удаления. Тем не менее, если пользователь установил более одного поставщика сведений о доступности для того же типа запись адреса, пользователя следует удалить эти поставщиков в порядке, обратном порядку установки (то есть, всегда удаление последних поставщика). В противном случае реестра могут указывать поставщика, который уже удалено. 
  
## <a name="api-components"></a>Компоненты API

Свободен/занят API включает в себя следующие компоненты:
  
### <a name="definitions"></a>Определения

- [Константы (занятости API)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Типы данных

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Интерфейсы

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    
