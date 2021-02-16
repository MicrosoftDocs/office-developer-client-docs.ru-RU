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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Представляет диалоговое окно, которое позволяет пользователю выбирать несколько форм и возвращает массив информационных объектов формы, описывая эти формы.
  
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

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of the displayed dialog box. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом переданных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _pszTitle_
  
> [in] Указатель на строку, которая содержит заголовок диалоговых окно. Если параметр  _pszTitle_ имеет значение NULL, поставщик библиотеки форм, который предоставляет формы, предоставляет заголовок по умолчанию. 
    
 _pfld_
  
> [in] Указатель на папку, из которой нужно выбрать формы. Если параметр  _pfld_ имеет NULL, формы выбираются из локального, личного или контейнера формы организации. 
    
 _pfrminfoarray_
  
> [in] Указатель на массив информационных объектов формы, предварительно выборки для пользователя.
    
 _ppfrminfoarray_
  
> [out] Указатель на указатель на возвращенный массив информационных объектов формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

С помощью метода **IMAPIFormMgr::SelectMultipleForms можно вызвать метод IMAPIFormMgr::SelectMultipleForms,** чтобы сначала представить диалоговое окно, которое позволяет пользователю выбирать несколько форм, а затем извлекать массив информационных объектов форм, которые описывают выбранные формы. В диалоговом окне **SelectMultipleForms** отображаются все формы независимо от того, являются ли они скрытыми (то есть понятны ли их скрытые свойства). 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если просмотр формы передает флаг MAPI_UNICODE в  _параметре ulFlags,_ все строки будут Юникод. Поставщики библиотеки форм, которые не поддерживают строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, MAPI_UNICODE передается. 
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

