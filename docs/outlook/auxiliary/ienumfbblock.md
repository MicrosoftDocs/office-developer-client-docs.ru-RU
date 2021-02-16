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

Поддерживает доступ к блокам данных о доступности и их нумерации для пользователя в течение задающегося диапазона времени.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследуется от:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Предоставлено:  <br/> |Поставщик услуг занятости  <br/> |
|Идентификатор интерфейса:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Возвращает следующее указанное количество блоков данных о занятости в этом перенамеровке.  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |Пропускает указанное количество блоков данных о занятости.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Сбрасывает enumerator, устанавливая курсор в начале.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Создает копию enumerator, используя то же ограничение времени, но устанавливая курсор в начале этого параметра.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Ограничивает его указанным периодом времени.  <br/> |
   
## <a name="remarks"></a>Примечания

Enumeration contains free/busy blocks of data that do not overlap in time. Если в календаре имеются перекрывающиеся элементы, Outlook объединяет эти элементы для формирования не перекрывающихся блоков занятости и занятости в порядке приоритета: "нет на офисе", "занят", "под вопросом".
  
Поставщик услуг занятости получает этот интерфейс и enumeration для диапазона времени для пользователя через [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>См. также

- [О доступности API](about-the-free-busy-api.md)  
- [Constants (Free/busy API)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

