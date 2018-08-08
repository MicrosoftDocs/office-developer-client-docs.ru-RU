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
ms.openlocfilehash: cb6138072cd5dedc528168d4056041661c40fd06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808675"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**Относится к**: Outlook 
  
Гарантирует, что метод **OpenEntry** открывается с ожидаемый Exchange доступа к адресной книге. Эта функция работает так же, [IAddrBook::Details](iaddrbook-details.md), но открывает **entryID** , с помощью адресная книга Exchange, определенного параметром _pEmsmdbUID_ . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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

## <a name="parameters"></a>Параметры

 _pmsess_
  
> Система на **IMAPISession**. Он не может быть NULL.
    
 _pEmsmdbUID_
  
> Указатель на **emsmdbUID** , который определяет службу Exchange, которая содержит поставщик адресной книги Exchange, которая используется для открытия идентификатор записи с помощью функции. Если входящий идентификатор записи не идентификатор записи адресной книги Exchange поставщика, этот параметр игнорируется и функцию действует как [IAddrBook::OpenEntry](iaddrbook-openentry.md). Если этот параметр имеет значение NULL или ноль **MAPIUID**, эта функция также работает так же, как [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] В адресной книге используется для открытия идентификатор записи. Он не может быть NULL.
    
 _lpulUIParam_
  
> [out] Дескриптор родительского окна для диалогового окна.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию, на основе **DISMISSMODELESS** прототип, или значение NULL. Этот член применим только к безрежимным версии диалоговом окне, указанной флагом DIALOG_SDI задаваемая. MAPI вызывает **DISMISSMODELESS** функцию, если пользователь не закрывает диалоговом окне безрежимным адреса клиента, который вызывает диалоговое окно не является активной подробные сведения о том. 
    
 _lpvDismissContext_
  
> [in] Указатель на сведения о контексте для передачи **DISMISSMODELESS** функции, с помощью параметра _lpfnDismiss_ . Этот параметр применяется только к безрежимным версии диалогового окна, включая флаг **DIALOG_SDI** с помощью параметра _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основании прототипа функции **LPFNBUTTON** . В функции **LPFNBUTTON** добавляется кнопка в диалоговом окне "Подробности". 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, используемый в качестве параметра для функции, указанного с помощью параметра _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Указатель на строку, которая содержит текст, который применяется для кнопки добавлены, если эта кнопка является расширяемым. Значение параметра _lpszButtonText_ должно быть значение NULL, когда расширяемая кнопка не требуется. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ . Можно задать следующие флажки: 
    
AB_TELL_DETAILS_CHANGE
  
> Указывает, что сведения о возвращает TRUE, если фактически изменений на адрес; в противном случае сведения о возвращает значение FALSE.
    
DIALOG_MODAL
  
> Отображает модальное версию стандартным диалоговым окном адрес. Этот флаг является взаимоисключающим с DIALOG_SDI.
    
DIALOG_SDI
  
> Отображает безрежимным версию стандартным диалоговым окном адрес. Этот флаг является взаимоисключающим с DIALOG_MODAL.
    
MAPI_UNICODE
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    

