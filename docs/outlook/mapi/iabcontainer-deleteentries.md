---
title: Иабконтаинерделетинтриес
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339384"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет одну или несколько записей, как правило, пользователи системы обмена сообщениями, списки рассылки или другие контейнеры.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _Лпентриес_
  
> возврата Указатель на массив структур [ентрилист](entrylist.md) , который содержит идентификаторы записей, представляющие удаляемые записи. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указанные записи были успешно удалены. 
    
МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН 
  
> Вызов выполнен успешно, но не удалось удалить одну или несколько записей. Когда возвращается это значение, вызов должен обрабатываться как успешный. Чтобы проверить это значение, используйте макрос **хр_фаилед** . Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Абдлг. cpp  <br/> |Кабдлг:: Онделетеселектедитем  <br/> |MFCMAPI использует метод **делетинтриес** для удаления определенной записи из контейнера адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

