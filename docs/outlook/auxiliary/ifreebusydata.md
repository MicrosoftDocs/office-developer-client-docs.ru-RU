---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: cd9d4dffd83e1995319b0f0d661435fedb78f28c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317502"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Для заданного пользователя получает и задает диапазон времени и возвращает интерфейс для нумерации блоков данных о занятости в пределах этого диапазона времени.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследуется от:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Предоставлено:  <br/> |Поставщик услуг занятости  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Получает интерфейс, который enumerates free/busy blocks of data for a user within a specified time range.  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Задает диапазон времени для enumeration of free/busy blocks of data for a user.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Получает заранее заранее задав диапазон времени для перенамерения блоков данных о занятости для пользователя.  <br/> |
   
## <a name="remarks"></a>Примечания

Большинство членов этого интерфейса являются замесятелями, зарезервированными для внутреннего использования Outlook, и могут изменяться. Поставщики услуг занятости должны реализовывать их только в указанном режиме, возвращая только указанные возвращаемые значения.
  
## <a name="see-also"></a>См. также

- [О доступности API](about-the-free-busy-api.md)
- [Constants (Free/busy API)](constants-free-busy-api.md)

