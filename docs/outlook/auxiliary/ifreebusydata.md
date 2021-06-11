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

Для данного пользователя получает и задает диапазон времени и возвращает интерфейс для перенамерения свободных и загруженных блоков данных в этом диапазоне времени.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Предоставлено:  <br/> |Бесплатный/занятый поставщик  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *Этот член является задатщиком и не поддерживается.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Получает интерфейс, который указывает свободные и загруженные блоки данных для пользователя в указанном диапазоне времени.  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *Этот член является задатщиком и не поддерживается.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Этот член является задатщиком и не поддерживается.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Этот член является задатщиком и не поддерживается.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Этот член является задатщиком и не поддерживается.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Задает диапазон времени для переумерия бесплатных и загруженных блоков данных для пользователя.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Этот член является задатщиком и не поддерживается.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Получает предустановленный диапазон времени для переустановки бесплатных и загруженных блоков данных для пользователя.  <br/> |
   
## <a name="remarks"></a>Примечания

Большинство участников этого интерфейса являются задатчиками, зарезервированными для внутреннего Outlook и подлежат изменениям. Поставщики бесплатных и занятых услуг должны реализовать их только в указанных значениях, возвращая только указанные значения возврата.
  
## <a name="see-also"></a>См. также

- [О доступности API](about-the-free-busy-api.md)
- [Константы (API free/busy)](constants-free-busy-api.md)

