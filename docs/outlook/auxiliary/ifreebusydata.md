---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: aa42561277d5fc4de93eeedec8ceb6f36530fb80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807720"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Для определенного пользователя, получает и задает диапазон времени и возвращает интерфейс для перечисления сведений о доступности блоков данных в пределах этого диапазона времени.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[Интерфейс IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Предоставлено:  <br/> |Обмен сведениями о доступности поставщика  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Прототип 1](ifreebusydata-placeholder1.md) <br/> | *Этот член — это и не поддерживается.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Получает интерфейс, который перечисляет занятости блоков данных для пользователя в рамках в заданном диапазоне времени.  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *Этот член — это и не поддерживается.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Этот член — это и не поддерживается.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Этот член — это и не поддерживается.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Этот член — это и не поддерживается.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Задает диапазон времени для перечисления блоков данных о доступности для пользователя.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Этот член — это и не поддерживается.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Получает указанного интервала времени для перечисления сведений о доступности блоков данных для пользователя.  <br/> |
   
## <a name="remarks"></a>Замечания

Большая часть члены этого интерфейса являются заполнители зарезервировано для внутреннего использования Outlook и могут быть изменены. Обмен сведениями о доступности поставщиков необходимо реализовать их только как указано, возвращение только указанного значения, возвращаемые.
  
## <a name="see-also"></a>См. также

- [About the Free/Busy API](about-the-free-busy-api.md)
- [Константы (занятости API)](constants-free-busy-api.md)

