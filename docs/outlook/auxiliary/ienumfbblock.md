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

Поддерживает доступ и перечисление блоков сведений о занятости для пользователя в диапазоне времени.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследование от:  <br/> |[Интерфейс](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Предоставлено:  <br/> |Поставщик сведений о доступности  <br/> |
|Идентификатор интерфейса:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Получает следующее указанное количество блоков данных о занятости в перечислении.  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |Пропускает указанное количество блоков данных о занятости.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Сбрасывает перечислитель, устанавливая курсор в начало.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Создает копию перечислителя с использованием того же ограничения времени, но устанавливая курсор в начало перечислителя.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Ограничит перечисление до указанного периода времени.  <br/> |
   
## <a name="remarks"></a>Примечания

Перечисление содержит блоки данных о занятости, которые не перекрываются в течение времени. При наличии перекрывающихся элементов в календаре Outlook выполняет слияние этих элементов для формирования неперекрывающихся блоков сведений о занятости в перечислении на основе следующего порядка приоритетов: "нет на месте", "занято" и "под вопросом".
  
Поставщик сведений о доступности получает этот интерфейс и перечисление для диапазона времени для пользователя с помощью [ифрибусидата](ifreebusydata.md).
  
## <a name="see-also"></a>См. также

- [О доступности API](about-the-free-busy-api.md)  
- [Константы (API сведений о доступности)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

