---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417646"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Не используйте эту функцию.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] Byte count of the entry identifier specified by the  _lpEntryID_ parameter. 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, который представляет открытую запись адресной книги.
    
 _lpInterface_
  
>  [in] Указатель на идентификатор интерфейса (IID) интерфейса, который будет использоваться для доступа к открытой записи. Передача NULL возвращает стандартный интерфейс объекта. Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md). Для списков рассылки это [IDistList: IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров — [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Звонители могут настроить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования. 
    
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
    
 _lpulObjType_
  
> [вышел] Указатель на тип открываемой записи.
    
 _lppUnk_
  
> [вышел] Указатель на указатель открываемой записи.
    

