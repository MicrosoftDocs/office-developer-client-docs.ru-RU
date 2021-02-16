---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Выполняет классификацию почтового элемента после отправки на основе его PidTagConversationId.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318902"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Выполняет категоризацию почтового элемента после отправки на основе [его PidTagConversationId.](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируется с помощью:  <br/> |Outlook.exe  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>Параметры

_pmbinStoreEid_
  
> [in] [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) магазина или [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) почтового элемента. Не может быть NULL или недопустимым. 
    
_pmbinMsgEid_
  
> [in] [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) почтового элемента. Не может быть NULL или недопустимым. 
    
_pmbinConvID_
  
> [in] [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) почтового элемента. Не может быть NULL или недопустимым. 
    
_dwFlags_
  
> [in] Битоваяmas, которая указывает дополнительные сведения о вызове метода.
    
   - 0 — в этом вызове метода не используются дополнительные параметры. Это рекомендуемое значение. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ фактически является [pidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) сообщения. Использование **PidTagSearchKey** ресурсоемко, и его следует избегать, [если доступен PidTagEntryId.](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов был успешным.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags содержит_ неизвестный флаг.  <br/> |
   
## <a name="remarks"></a>Примечания

Категории считаются персональными данными и не должны передаваться за пределы почтового ящика пользователя. Поэтому не вызывайте **HrProcessConvActionForSentItem** для элемента неподдерживаемой почты. Вместо этого отправьте элемент, а затем вызовите **HrProcessConvActionForSentItem** в архивной копии. Архивная копия может храниться в папке "Отправленные" или в эквивалентном расположении. 
  
Для вызова **HrProcessConvActionForSentItem** приложение должно быть в процессе Outlook.exe, например из надстройки COM. Если попытаться вызвать **HrProcessConvActionForSentItem** вне процесса, **HrProcessConvActionForSentItem выдает** исключение нарушения доступа. 
  

