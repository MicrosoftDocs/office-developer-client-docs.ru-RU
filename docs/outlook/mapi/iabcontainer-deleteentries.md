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
ms.openlocfilehash: 4140dc39b7f866b0372e5940aef5efc0524ad593
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573112"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

