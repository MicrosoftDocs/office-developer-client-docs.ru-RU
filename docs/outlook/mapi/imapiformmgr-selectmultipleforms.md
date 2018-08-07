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
ms.openlocfilehash: 096437f10c5b992a1db55f6a856c38021a81b99a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808960"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**Относится к**: Outlook 
  
Предоставляет диалоговое окно, которое позволяет пользователю выбрать нескольких форм и возвращает массив формы объекты, которые описывают формах.
  
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
  
> [in] Дескриптор родительского окна, отображаемого диалогового окна. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип строк, переданное. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _pszTitle_
  
> [in] Указатель на строку, которая содержит заголовок диалогового окна. Если параметр _pszTitle_ имеет значение NULL, поставщик библиотеки форм, предоставляющий форм предоставляет заголовок по умолчанию. 
    
 _pfld_
  
> [in] Указатель на папку для выбора формы. Если параметр _pfld_ имеет значение NULL, формы выбираются из контейнера формы local, личный или организации. 
    
 _pfrminfoarray_
  
> [in] Указатель на массив объектов формы сведения, которые предварительно выбранных для пользователя.
    
 _ppfrminfoarray_
  
> [out] Указатель на указатель на возвращаемый массив объектов данные формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Средства просмотра формы вызвать метод **IMAPIFormMgr::SelectMultipleForms** для первым диалоговое окно, которое позволяет пользователю выбрать нескольких форм нажмите для получения массива формы сведения объекты и, описывающие выбранные формы. Диалоговое окно **SelectMultipleForms** отображает все формы ли они являются скрытыми (то есть ли их скрытые свойства не установлены). 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если форма просмотра передает флаг MAPI_UNICODE в параметре _ulFlags_ , все строки содержат Юникод. Поставщики библиотеки форм, которые не поддерживают строк в кодировке Юникод должен возвращать MAPI_E_BAD_CHARWIDTH, если передается MAPI_UNICODE. 
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

