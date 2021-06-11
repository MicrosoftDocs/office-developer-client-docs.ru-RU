---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426781"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
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
  
> [вышел] Указатель на ручку родительского окна возвращаемого диалогового окна.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию на основе прототипа [DISMISSMODELESS](dismissmodeless.md) или NULL. Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге. MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адреса, информируя клиента, который вызывает **IMAPISupport::D etails,** что диалоговое окно больше не активен. 
    
 _lpvDismissContext_
  
> [in] Указатель для контекстной информации, чтобы передать функции **DISMISSMODELESS,** указываемую _параметром lpfnDismiss._ Этот параметр применяется только к бесключевой версии диалогового окна, включив флаг DIALOG_SDI в параметр _ulFlags._ 
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, для которого отображаются сведения.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основе прототипа [функции LPFNBUTTON.](lpfnbutton.md) Функция **LPFNBUTTON добавляет** кнопку в диалоговое окно подробностей. 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, используемые в качестве параметра для функции, указанной _параметром lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Указатель на строку, содержавшую текст, который будет применяться к добавленной кнопке, если эта кнопка является размежещенной. Параметр  _lpszButtonText должен_ быть NULL, если не требуется размягкаемая кнопка. 
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют тип текста для _параметра lpszButtonText._ Можно установить следующий флаг: 
    
DIALOG_MODAL
  
> Отображение модальной версии диалогового окна общего адреса. Этот флаг является взаимоисключающими с DIALOG_SDI.
    
DIALOG_SDI
  
>  Отображение бес режимной версии диалогового окна общего адреса. Этот флаг является взаимоисключающими с DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> Переданные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Диалоговое окно с подробными сведениями было успешно отображно для записи адресной книги.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::D etails** реализован для объектов поддержки поставщиков адресных книг. Поставщики адресных книг **звонят в Details,** чтобы отобразить диалоговое окно, в которое будут представлены сведения о конкретной записи в адресной книге. Параметры  _lpfButtonCallback,_  _lpvButtonContext_ и  _lpszButtonText_ можно использовать для добавления кнопки, определенной клиентом, в диалоговое окно. При нажатии кнопки MAPI вызывает функцию вызова, указанную  _lpfButtonCallback,_ передавая как идентификатор входа кнопки, так и данные  _в lpvButtonContext_. Если не требуется размягкаемая кнопка,  _lpszButtonText_ должен быть NULL. 
  
## <a name="see-also"></a>См. также



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

