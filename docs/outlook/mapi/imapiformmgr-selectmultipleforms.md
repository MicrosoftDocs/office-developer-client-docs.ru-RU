---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420313"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет диалоговое окно, которое позволяет пользователю выбирать несколько форм и возвращает массив объектов информации о форме, описывая эти формы.
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна отображаемого диалогового окна. 
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом переданных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 _pszTitle_
  
> [in] Указатель на строку, содержаную подпись диалогового окна. Если параметр  _pszTitle_ — NULL, поставщик библиотеки форм, который предоставляет формы, содержит подпись по умолчанию. 
    
 _pfld_
  
> [in] Указатель на папку, из которой нужно выбрать формы. Если параметр  _pfld_ является NULL, формы выбираются из локального, личного или контейнера формы организации. 
    
 _pfrminfoarray_
  
> [in] Указатель на массив объектов информации о форме, предварительно предварительно отбираемых для пользователя.
    
 _ppfrminfoarray_
  
> [вышел] Указатель на указатель возвращаемого массива информационных объектов форм.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIFormMgr:::SelectMultipleForms,** чтобы сначала представить диалоговое окно, которое позволяет пользователю выбрать несколько форм, а затем получить массив информационных объектов форм, описывая выбранные формы. Диалоговое окно **SelectMultipleForms** отображает все формы независимо от того, скрыты ли они (то есть понятны ли их скрытые свойства). 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если зритель формы передает флаг MAPI_UNICODE  _в параметре ulFlags,_ все строки являются Юникодом. Поставщики библиотек форм, которые не поддерживают строки Юникод, должны MAPI_E_BAD_CHARWIDTH, если MAPI_UNICODE будет пройдена. 
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

