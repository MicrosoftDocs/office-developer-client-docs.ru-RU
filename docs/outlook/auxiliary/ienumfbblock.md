---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317628"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Поддерживает доступ и переумеживающие свободные и загруженные блоки данных для пользователя в пределах диапазона времени.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Предоставлено:  <br/> |Бесплатный/занятый поставщик  <br/> |
|Идентификатор интерфейса:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Получает следующее указанное количество блоков бесплатных и загруженных данных в переумериях.  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |Пропускает указанное количество блоков бесплатных и загруженных данных.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Сбрасывает переустановку, установив курсор к началу.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Создает копию этого перемерителя, используя одно и то же ограничение времени, но устанавливая курсор к началу этого.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Ограничивает указанный период времени.  <br/> |
   
## <a name="remarks"></a>Примечания

В переумериях содержатся свободные и загруженные блоки данных, которые не совпадают во времени. Если в календаре есть перекрывающиеся элементы, Outlook объединяет эти элементы, чтобы сформировать не перекрывающиеся свободные и занятые блоки в переумериях на основе этого порядка приоритета: вне офиса, занят, предварительно.
  
Бесплатный/занятый поставщик получает этот интерфейс и переумежение для диапазона времени для пользователя через [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>См. также

- [О доступности API](about-the-free-busy-api.md)  
- [Константы (API free/busy)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

