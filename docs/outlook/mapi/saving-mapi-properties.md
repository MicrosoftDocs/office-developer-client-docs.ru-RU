---
title: Сохранение свойств MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812172"
---
# <a name="saving-mapi-properties"></a>Сохранение свойств MAPI

  
  
**Применимо к**: Outlook 
  
Многие объекты поддержки модели транзакций обработки посредством изменения свойств не становятся постоянной до момента фиксации в дальнейшем. В то время как изменения свойства обрабатываются с помощью методов [IMAPIProp::SetProps](imapiprop-setprops.md) и [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , действие фиксации обрабатывается [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Файл не является только после успешного вызова **SaveChanges** , что можно получить доступ к наиболее поздней версии для свойств объектов. 
  
Когда **SaveChanges** возвращает значение ошибки MAPI_E_OBJECT_CHANGED, это предупреждение, что другой клиент одновременно внесением изменений на объект. Возможно, в зависимости от поставщика, реализация объекта для нескольких клиентов, чтобы успешно откройте объект путем вызова метода **OpenEntry** с установленным флагом MAPI_MODIFY, предоставляя доступ на чтение и запись. Объект, который возвращается из таких, что на вызов **OpenEntry** — моментальный снимок данных хранилища. Каждый повторная попытка изменить эти данные можно перезаписать Предыдущая попытка. 
  
При получении MAPI_E_OBJECT_CHANGED от **SaveChanges**, клиент имеет возможность: 
  
- Создайте копию объекта для сохранения изменений.
    
- Сделайте другой вызов **SaveChanges**, определяющее FORCE_SAVE. 
    
При вызове **SaveChanges** флаг FORCE_SAVE перезаписывает предыдущей сохранить и внесите необходимые изменения клиента было постоянным. 
  
## <a name="see-also"></a>См. также



[Обзор свойств MAPI](mapi-property-overview.md)

