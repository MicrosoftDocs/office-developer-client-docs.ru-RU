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
ms.openlocfilehash: 9923813d821e2b34497e3b498c19ce22ceda2eb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809105"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
**Относится к**: Outlook 
  
Отображает диалоговое окно, которое предоставляет подробные сведения о записи определенного адресной книги.
  
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
  
> [out] Указатель на дескриптор родительского окна, возвращенные диалогового окна.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию, на основе [DISMISSMODELESS](dismissmodeless.md) прототип, или значение NULL. Этот член применим только к безрежимным версии диалоговом окне, указанной флагом DIALOG_SDI задаваемая. MAPI вызывает **DISMISSMODELESS** функцию, если пользователь не закрывает диалоговое окно безрежимным адрес, уведомляющее о клиента, который вызывает **IMAPISupport::Details** диалоговое окно не является активной. 
    
 _lpvDismissContext_
  
> [in] Указатель на сведения о контексте для передачи **DISMISSMODELESS** функции, с помощью параметра _lpfnDismiss_ . Этот параметр применяется только к безрежимным версии диалоговом окне, включая флаг DIALOG_SDI с помощью параметра _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, для которого отображаются подробные сведения.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основании прототипа функции [LPFNBUTTON](lpfnbutton.md) . В функции **LPFNBUTTON** добавляется кнопка в диалоговом окне "Подробности". 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, используемые как параметр для функции, указанного с помощью параметра _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Указатель на строку, которая содержит текст, который будет применяться к добавлена кнопка Если кнопки является расширяемым. Параметр _lpszButtonText_ должен иметь значение NULL, если расширяемая кнопка не требуется. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ . Можно задать следующий флаг: 
    
DIALOG_MODAL
  
> Отображение модального версии стандартным диалоговым окном адрес. Этот флаг является взаимоисключающим с DIALOG_SDI.
    
DIALOG_SDI
  
>  Отображение безрежимным версии стандартным диалоговым окном адрес. Этот флаг является взаимоисключающим с DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Для записи адресной книги был успешно отображается диалоговое окно "Подробности".
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::Details** реализуется для объектов поддержки поставщик адресной книги. Поставщиками адресной книги вызовите **сведений** для отображения диалогового окна, подробные сведения о конкретной записи в адресной книге. Параметры _lpfButtonCallback_, _lpvButtonContext_и _lpszButtonText_ можно использовать для добавления кнопки определенные клиента в диалоговое окно. При нажатии кнопки MAPI вызывает функцию обратного вызова, на который указывает _lpfButtonCallback_, передав запись идентификатора кнопки и данные в _lpvButtonContext_. Если не требуется расширяемая кнопка, _lpszButtonText_ должен иметь значение NULL. 
  
## <a name="see-also"></a>См. также



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

