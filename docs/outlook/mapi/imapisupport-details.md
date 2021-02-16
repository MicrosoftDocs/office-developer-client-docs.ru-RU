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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно с подробными сведениями об определенной записи адресной книги.
  
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

## <a name="parameters"></a>Параметры

 _lpulUIParam_
  
> [out] Указатель на ладработку родительского окна возвращенного диалогового окна.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию на основе [прототипа DISMISSMODELESS](dismissmodeless.md) или NULL. Этот член применяется только к неавтомантной версии диалогового окна, как указано DIALOG_SDI флагом. MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адресов, сообщая клиенту, который вызывает **IMAPISupport::D etails,** что диалоговое окно больше не активно. 
    
 _lpvDismissContext_
  
> [in] Указатель на контекстную информацию, которая передается функции **DISMISSMODELESS,** на которую указывает параметр _lpfnDismiss._ Этот параметр применяется только к безмежной версии диалоговых окна, включив флаг DIALOG_SDI в параметр _ulFlags._ 
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, для которого отображаются сведения.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основе прототипа [функции LPFNBUTTON.](lpfnbutton.md) Функция **LPFNBUTTON** добавляет кнопку в диалоговое окно сведений. 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, используемые в качестве параметра для функции, указанной параметром _lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Указатель на строку, содержаную текст, который будет применен к добавленной кнопке, если эта кнопка является выдержатой. Параметр  _lpszButtonText должен_ иметь NULL, если вы не хотите использовать эту кнопку. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._ Можно установить следующий флаг: 
    
DIALOG_MODAL
  
> Отображение модальной версии общего диалоговых окна адресов. Этот флаг является взаимоисключающими с DIALOG_SDI.
    
DIALOG_SDI
  
>  Отображает неавтомтную версию общего диалоговых окна адресов. Этот флаг является взаимоисключающими с DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Диалоговое окно сведений успешно отобразилось для записи адресной книги.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::D etails** реализован для объектов поддержки поставщика адресной книги. Поставщики адресных книг **звонят** в "Сведения", чтобы отобразить диалоговое окно с подробными сведениями об определенной записи в адресной книге. Параметры  _lpfButtonCallback,_  _lpvButtonContext_ и  _lpszButtonText_ можно использовать для добавления в диалоговое окно определяемой клиентом кнопки. При нажатии кнопки MAPI вызывает функцию вызова, на которая указывает _lpfButtonCallback,_ передавая идентификатор записи кнопки и данные _в lpvButtonContext._ Если вы не хотите использовать эту кнопку,  _lpszButtonText_ должен иметь NULL. 
  
## <a name="see-also"></a>См. также



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

