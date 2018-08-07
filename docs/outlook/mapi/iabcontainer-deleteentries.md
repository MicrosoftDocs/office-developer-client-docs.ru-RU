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
ms.openlocfilehash: c744407790fecde6b6d89dff669ea4db07ce7701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808707"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Относится к**: Outlook 
  
Удаляет один или несколько операций, обычно системы обмена сообщениями пользователи, списков рассылки или других контейнеров.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpEntries_
  
> [in] Указатель на массив структур [ENTRYLIST](entrylist.md) , которые содержат идентификаторы записей, которые представляют операции удаления. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Указанные записи успешно удален. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов завершился успешно, но не удалось удалить один или несколько записей. При возвращении это значение вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это значение, используйте макрос **HR_FAILED** . Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |Mfcmapi (en) метод **внешнее** используется для удаления конкретную запись из контейнер адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

