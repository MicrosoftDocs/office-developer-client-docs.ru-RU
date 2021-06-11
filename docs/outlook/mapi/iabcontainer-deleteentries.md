---
title: IABContainerDeleteEntries
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425598"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет одну или несколько записей, как правило, пользователей сообщений, списки рассылки или другие контейнеры.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpEntries_
  
> [in] Указатель на массив структур [ENTRYLIST,](entrylist.md) содержащих идентификаторы записей, которые представляют удаленные записи. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указанные записи успешно удалены. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов удался, но одну или несколько записей не удалось удалить. Когда это значение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это значение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI использует метод **DeleteEntries** для удаления определенной записи из контейнера адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

