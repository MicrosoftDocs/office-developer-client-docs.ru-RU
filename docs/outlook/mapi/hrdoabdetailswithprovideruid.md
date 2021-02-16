---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426683"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Обеспечивает открытие метода **OpenEntry** ожидаемым поставщиком адресной книги Exchange. Эта функция работает аналогично [IAddrBook::D etails,](iaddrbook-details.md) но открывает **entryID** с помощью адресной книги Exchange, определенной _pEmsabpUID._
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a>Параметры

 _pEmsabpUID_
  
> [in] Указатель на  _emsabpUID,_ идентифицирует поставщика адресной книги Exchange, который эта функция должна использовать для отображения сведений об идентификаторе записи. Если идентификатор входной записи не является идентификатором записи поставщика адресной книги Exchange, этот параметр игнорируется, и вызов функции действует точно так же, как [IAddrBook::D etails](iaddrbook-details.md). Если этот параметр имеет значение NULL или mapIUID нулевого уровня, эта функция также действует точно так же, как [IAddrBook::D etails.](iaddrbook-details.md)
    
 _pAddrBook_
  
> [in] Адресная книга, используемая для открытия идентификатора записи. Это не может быть NULL.
    
 _lpulUIParam_
  
> [out] Handle to the parent window for the dialog box.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию на основе **прототипа DISMISSMODELESS** или NULL. Этот член применяется только к неавтомантной версии диалогового окна, как указано DIALOG_SDI флага. MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адресов, сообщая клиенту, который вызывает details, о том, что диалоговое окно больше не активно. 
    
 _lpvDismissContext_
  
> [in] Указатель на контекстную информацию, которая передается функции **DISMISSMODELESS,** на которую указывает параметр _lpfnDismiss._ Этот параметр применяется только к неавтомантной версии  диалоговых окно, включив флаг DIALOG_SDI в параметр _ulFlags._ 
    
 _cbEntryID_
  
> [in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основе прототипа **функции LPFNBUTTON.** Функция **LPFNBUTTON** добавляет кнопку в диалоговое окно сведений. 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, которые использовались в качестве параметра для функции, указанной параметром _lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Указатель на строку, содержаную текст, который необходимо применить к добавленной кнопке, если эта кнопка является выдержатой. Параметр  _lpszButtonText должен_ иметь NULL, если не требуется размягкаемая кнопка. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._ Можно установить следующие флаги: 
    
AB_TELL_DETAILS_CHANGE
  
> Указывает, что details возвращает true, если фактически в адрес были внесены изменения; в противном случае details возвращает false.
    
DIALOG_MODAL
  
> Отображает модальные версии общего диалоговых окна адресов. Этот флаг является взаимоисключающими с DIALOG_SDI.
    
DIALOG_SDI
  
> Отображает неавтомтную версию общего диалоговых окна адресов. Этот флаг является взаимоисключающими с DIALOG_MODAL.
    
MAPI_UNICODE
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    

