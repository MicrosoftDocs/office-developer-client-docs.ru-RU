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
  
> [in] Указатель на окне родительского окна для диалоговых окон.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию на основе [прототипа DISMISSMODELESS](dismissmodeless.md) или NULL. Этот член применяется только к неавтомантной версии диалогового окна, как указано DIALOG_SDI флага. MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без  режима адресов, сообщая клиенту, который вызывает details, о том, что диалоговое окно больше не активно. 
    
 _lpvDismissContext_
  
> [in] Указатель на контекстную информацию, которая передается функции **DISMISSMODELESS,** на которую указывает параметр _lpfnDismiss._ Этот параметр применяется только к безмежной версии диалоговых окна, включив флаг DIALOG_SDI в параметр _ulFlags._ 
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, для которой отображаются сведения.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основе прототипа [функции LPFNBUTTON.](lpfnbutton.md) Функция **LPFNBUTTON** добавляет кнопку в диалоговое окно сведений. 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, которые использовались в качестве параметра для функции, указанной параметром _lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Указатель на строку, содержаную текст, который необходимо применить к добавленной кнопке, если эта кнопка является выдержатой. Параметр  _lpszButtonText_ должен иметь NULL, если не требуется кнопка с возможностью". 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._ Можно установить следующие флаги: 
    
AB_TELL_DETAILS_CHANGE
  
> Указывает, что **подробные** сведения S_OK, если фактически были внесены изменения в адрес; в **противном случае details** возвращает S_FALSE. 
    
DIALOG_MODAL
  
> Отображение модальной версии общего диалоговых окна адресов, которая всегда отображается в клиентах, не в которых используется Outlook. Этот флаг является взаимоисключающими с DIALOG_SDI.
    
DIALOG_SDI
  
>  Отображает неавтомтную версию общего диалоговых окна адресов. Этот флаг игнорируется для клиентов, не в том случае, если они не являются клиентами Outlook. 
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Диалоговое окно сведений успешно отобразилось для записи адресной книги.
    
## <a name="remarks"></a>Примечания

Клиентские приложения **звонят методу Details,** чтобы отобразить диалоговое окно с подробными сведениями об определенной записи в адресной книге. Для добавления в диалоговое окно определяемой клиентом кнопки можно использовать параметры _lpfButtonCallback,_ _lpvButtonContext_ и _lpszButtonText._ При нажатии кнопки MAPI вызывает функцию вызова, на которая указывает  _lpfButtonCallback,_ передавая идентификатор записи кнопки и данные  _в lpvButtonContext_. Если вы не хотите использовать эту кнопку,  _lpszButtonText_ должен иметь NULL. 
  
 **Подробные** сведения поддерживают строки символов Юникода; Строки Юникода преобразуются в формат многобайтовых строк (MBCS) перед их отображением в диалоговом окне сведений. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI использует метод **Details,** чтобы отобразить диалоговое окно с подробными сведениями о записи адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

