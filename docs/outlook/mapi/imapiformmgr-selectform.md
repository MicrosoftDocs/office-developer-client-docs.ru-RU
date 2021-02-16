---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423582"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Представляет диалоговое окно, которое позволяет пользователю выбрать форму, и возвращает объект сведений о форме, описывая эту форму.
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
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
  
> [in] Указатель на строку, которая содержит заголовок диалоговых окна. Если параметр  _pszTitle_ имеет значение NULL, поставщик библиотеки форм передает заголовок по умолчанию. 
    
 _pfld_
  
> [in] Указатель на папку, из которой нужно выбрать форму. Если параметр  _pfld_ имеет NULL, форму можно выбрать из локального, личного или контейнера формы организации. 
    
 _ppfrminfoReturned_
  
> [out] Указатель на указатель на возвращенный объект сведений формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Посетители форм вызовите метод **IMAPIFormMgr::SelectForm,** чтобы сначала представить диалоговое окно, которое позволяет пользователю выбрать форму, а затем получить объект сведений о форме, описывая выбранную форму. Диалоговое окно ограничивает выбор одной формы пользователем. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В **диалоговом окне SelectForm** отображаются только те формы, которые не являются скрытыми (то есть формы со скрытыми свойствами не скрыты). Если просмотр формы передает флаг MAPI_UNICODE в  _параметре ulFlags,_ все строки будут Юникод. Поставщики библиотеки форм, которые не поддерживают строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, MAPI_UNICODE передается. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI использует метод **IMAPIFormMgr::SelectForm** для выбора формы и отправки сведений о форме в один или несколько журналов.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

