---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421370"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Гарантирует, что метод **OpenEntry** откроется ожидаемым поставщиком Exchange адресной книги. Эта функция работает аналогично [IAddrBook::D etails,](iaddrbook-details.md)но открывает **entryID** с помощью Exchange адресной книги, определенной _параметром pEmsmdbUID._ 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a>Parameters

 _pmsess_
  
> Журнал на **IMAPISession**. Это не может быть NULL.
    
 _pEmsmdbUID_
  
> Указатель на **emsmdbUID,** который определяет службу Exchange, которая содержит поставщик Exchange адресной книги, который используется функцией для открытия идентификатора записи. Если идентификатор входной записи не является идентификатором записи поставщика Exchange адресной книги, этот параметр игнорируется, и функция ведет себя как [IAddrBook::OpenEntry](iaddrbook-openentry.md). Если этот параметр NULL или нулевой **MAPIUID,** эта функция также действует точно так же, как [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] Адресная книга, используемая для открытия идентификатора записи. Это не может быть NULL.
    
 _lpulUIParam_
  
> [вышел] Ручка родительского окна для диалоговое окно.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию на основе прототипа **DISMISSMODELESS** или NULL. Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге. MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адреса, информируя клиента, который вызывает Details, что диалоговое окно больше не активен. 
    
 _lpvDismissContext_
  
> [in] Указатель для контекстной информации, чтобы передать функции **DISMISSMODELESS,** указываемую _параметром lpfnDismiss._ Этот параметр применяется только к бесключевой версии диалогового окна, включив **флаг** DIALOG_SDI в _параметр ulFlags._ 
    
 _cbEntryID_
  
> [in] Byte count of the entry identifier specified by the  _lpEntryID_ parameter. 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, который представляет открытую запись адресной книги.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основе прототипа **функции LPFNBUTTON.** Функция **LPFNBUTTON добавляет** кнопку в диалоговое окно подробностей. 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, которые использовались в качестве параметра для функции, указанной _параметром lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Указатель на строку, содержавшую текст, который необходимо применить к добавленной кнопке, если эта кнопка является размежещенной. Параметр  _lpszButtonText должен_ быть NULL, если не требуется размягкаемая кнопка. 
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют тип текста для _параметра lpszButtonText._ Можно установить следующие флаги: 
    
AB_TELL_DETAILS_CHANGE
  
> Указывает, что Details возвращает TRUE, если на самом деле в адрес внесены изменения; в противном случае Details возвращает FALSE.
    
DIALOG_MODAL
  
> Отображает модную версию диалогового окна общего адреса. Этот флаг является взаимоисключающими с DIALOG_SDI.
    
DIALOG_SDI
  
> Отображает бес режимную версию диалогового окна общего адреса. Этот флаг является взаимоисключающими с DIALOG_MODAL.
    
MAPI_UNICODE
  
> Переданные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    

