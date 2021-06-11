---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424681"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно, в которое отображаются сведения о конкретной записи адресной книги.
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulUIParam_
  
> [in] Указатель на ручку родительского окна диалоговое окно.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию на основе прототипа [DISMISSMODELESS](dismissmodeless.md) или NULL. Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге. MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без  режима адреса, информируя клиента, который вызывает Details, что диалоговое окно больше не активен. 
    
 _lpvDismissContext_
  
> [in] Указатель для контекстной информации, чтобы передать функции **DISMISSMODELESS,** указываемую _параметром lpfnDismiss._ Этот параметр применяется только к бесключевой версии диалогового окна, включив флаг DIALOG_SDI в параметр _ulFlags._ 
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для записи, для которой отображаются сведения.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основе прототипа [функции LPFNBUTTON.](lpfnbutton.md) Функция **LPFNBUTTON добавляет** кнопку в диалоговое окно подробностей. 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, которые использовались в качестве параметра для функции, указанной _параметром lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Указатель на строку, содержавшую текст, который необходимо применить к добавленной кнопке, если эта кнопка является размежещенной. Параметр  _lpszButtonText должен_ быть NULL, если вам не нужна неопределяемая кнопка. 
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют тип текста для _параметра lpszButtonText._ Можно установить следующие флаги: 
    
AB_TELL_DETAILS_CHANGE
  
> Указывает, что **details** возвращает S_OK, если на самом деле в адрес внесены изменения; в **противном** случае Details возвращает S_FALSE. 
    
DIALOG_MODAL
  
> Отображение модальной версии диалогового окна общего адреса, которое всегда отображается в Outlook клиентах. Этот флаг является взаимоисключающими с DIALOG_SDI.
    
DIALOG_SDI
  
>  Отображение бес режимной версии диалогового окна общего адреса. Этот флаг игнорируется для Outlook клиентов. 
    
MAPI_UNICODE 
  
> Переданные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Диалоговое окно с подробными сведениями было успешно отображно для записи адресной книги.
    
## <a name="remarks"></a>Примечания

Клиентские приложения звонят **методу Details,** чтобы отобразить диалоговое окно, которое содержит сведения о конкретной записи в адресной книге. Параметры  _lpfButtonCallback,_  _lpvButtonContext_ и  _lpszButtonText_ можно использовать для добавления кнопки, определенной клиентом, в диалоговое окно. При нажатии кнопки MAPI вызывает функцию вызова, указанную  _lpfButtonCallback,_ передавая как идентификатор входа кнопки, так и данные  _в lpvButtonContext_. Если вам не нужна неопределяемая кнопка,  _lpszButtonText_ должен быть NULL. 
  
 **Сведения** поддерживают строки символов Юникод; Строки Юникод преобразуются в формат многобайтной строки символов (MBCS) перед их отображением в диалоговом окне подробностей. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI использует метод **Details** для отображения диалоговое окно, в которое отображаются сведения для записи адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

