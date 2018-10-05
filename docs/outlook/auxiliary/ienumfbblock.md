---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388191"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Поддерживает доступ к и перечисление занятости блоков данных для пользователя в интервал времени.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[Интерфейс IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Предоставлено:  <br/> |Обмен сведениями о доступности поставщика  <br/> |
|Идентификатор интерфейса:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Далее](ienumfbblock-next.md) <br/> |Получает указанное количество блоков данных о доступности в перечислении.  <br/> |
|[Пропустить](ienumfbblock-skip.md) <br/> |Пропускает указанное число блоков данных о доступности.  <br/> |
|[Reset (Сбросить)](ienumfbblock-reset.md) <br/> |Сбрасывает перечислитель путем установки курсора в начало.  <br/> |
|[Копия](ienumfbblock-clone.md) <br/> |Создает копию перечислителя, с помощью же ограничения времени, но установки курсора в начало перечислитель.  <br/> |
|[Ограничить](ienumfbblock-restrict.md) <br/> |Ограничивает число перечисления для заданного периода времени.  <br/> |
   
## <a name="remarks"></a>Замечания

Перечисление содержит занятости блоки данных, которые не пересекаются в времени. Если есть перекрывающиеся элементы календаря, Outlook объединяет эти элементы для без перекрытия блоков сведений о доступности в перечисление, основанное на этом приоритет: документов office, «занят», под вопросом.
  
Обмен сведениями о доступности поставщика получает этот интерфейс и перечисления для интервала времени для пользователя через [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>См. также

- [About the Free/Busy API](about-the-free-busy-api.md)  
- [Константы (занятости API)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

