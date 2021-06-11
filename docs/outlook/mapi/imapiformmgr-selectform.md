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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет диалоговое окно, которое позволяет пользователю выбрать форму, и возвращает объект информации о форме, описывая эту форму.
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
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
  
> [in] Указатель на строку, содержаную подпись диалогового окна. Если параметр  _pszTitle_ является NULL, поставщик библиотеки форм поставляет подпись по умолчанию. 
    
 _pfld_
  
> [in] Указатель на папку, из которой нужно выбрать форму. Если параметр  _pfld_ NULL, форма может быть выбрана из локального, личного или контейнера формы организации. 
    
 _ppfrminfoReturned_
  
> [вышел] Указатель на указатель на возвращенный информационный объект формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIFormMgr:::SelectForm,** чтобы сначала представить диалоговое окно, которое позволяет пользователю выбрать форму, а затем получить информационный объект формы, описывая выбранную форму. Диалоговое окно ограничивает пользователя в выборе одной формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В **диалоговом** окне SelectForm отображаются только не скрытые формы (то есть формы со скрытыми свойствами). Если зритель формы передает флаг MAPI_UNICODE  _в параметре ulFlags,_ все строки являются Юникодом. Поставщики библиотек форм, которые не поддерживают строки Юникод, должны MAPI_E_BAD_CHARWIDTH, если MAPI_UNICODE будет пройдена. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI использует **метод IMAPIFormMgr::SelectForm** для выбора формы и отправки сведений о форме в один или несколько журналов.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

