---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Выполняет категоризацию после отправки для почтового элемента на основе его Пидтагконверсатионид.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318902"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Выполняет категоризацию после отправки для почтового элемента на основе его [пидтагконверсатионид](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировано:  <br/> |Outlook. exe  <br/> |
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

_Пмбинсториид_
  
> возврата [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) хранилища или [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) почтового элемента. Не может иметь значение NULL или быть недопустимым. 
    
_Пмбинмсжеид_
  
> возврата [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) почтового элемента. Не может иметь значение NULL или быть недопустимым. 
    
_Пмбинконвид_
  
> возврата [Пидтагконверсатионид](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) почтового элемента. Не может иметь значение NULL или быть недопустимым. 
    
_dwFlags_
  
> возврата Битовая маска, указывающая дополнительные сведения о вызове метода.
    
   - 0 — в этом вызове метода не используются дополнительные параметры. Это рекомендуемое значение. 
    
   - **Пкафсиф_мсжеид_ис_сеарч_кэй**— _Пмбинмсжеид_ фактически является [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) сообщения. Использование **PidTagSearchKey** является трудоемким и его следует избегать, если доступен [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_ содержит неизвестный флаг.  <br/> |
   
## <a name="remarks"></a>Замечания

Категории считаются персональными сведениями и не должны передаваться вне почтового ящика пользователя. Поэтому не вызывайте **хрпроцессконвактионфорсентитем** для неотправленного почтового элемента. Вместо этого отправьте элемент, а затем вызовите **хрпроцессконвактионфорсентитем** для архивной копии. Архивная копия может храниться в папке "Отправленные" или в эквивалентном расположении. 
  
Приложение должно быть в процессе работы с Outlook. exe, например из надстройки COM, для вызова **хрпроцессконвактионфорсентитем**. Если вы попытаетесь вызвать **хрпроцессконвактионфорсентитем** вне процесса, **хрпроцессконвактионфорсентитем** выдаст исключение нарушения прав доступа. 
  

