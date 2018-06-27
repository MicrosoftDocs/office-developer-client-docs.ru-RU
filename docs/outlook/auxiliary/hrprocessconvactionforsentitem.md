---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Выполняет категоризации после отправки почтового элемента на основании его PidTagConversationId.
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807708"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Выполняет категоризации после отправки почтового элемента на основании его [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |Outlook.exe  <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>Parameters

_pmbinStoreEid_
  
> [in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) хранилище или [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) из почтового элемента. Не может быть NULL или недопустимые. 
    
_pmbinMsgEid_
  
> [in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) почтового элемента. Не может быть NULL или недопустимые. 
    
_pmbinConvID_
  
> [in] [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) почтового элемента. Не может быть NULL или недопустимые. 
    
_dwFlags_
  
> [in] Битовая маска, которая указывает Дополнительные сведения о вызове метода.
    
   - 0 — Дополнительные параметры не используются в вызове этого метода. Это рекомендуемое значение. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ — это фактически [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) сообщения. С помощью **PidTagSearchKey** интенсивно и следует избегать при наличии [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |Вызов выполнен успешно.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_ содержит неизвестное флаг.  <br/> |
   
## <a name="remarks"></a>Замечания

Категории считаются персональные данные и не будут передаваться за пределами почтового ящика пользователя. Таким образом не вызывать **HrProcessConvActionForSentItem** неотправленные почтового элемента. Вместо этого отправить элемент, а затем вызвать **HrProcessConvActionForSentItem** на резервной копии. Архивные копии могут храниться в папке «Отправленные» или соответствующее место. 
  
Ваше приложение не должно содержать в работе с Outlook.exe, например, из надстройки COM, чтобы вызвать **HrProcessConvActionForSentItem**. При попытке вызова **HrProcessConvActionForSentItem** ожидания процесс **HrProcessConvActionForSentItem** вызовет исключение нарушение прав доступа. 
  
