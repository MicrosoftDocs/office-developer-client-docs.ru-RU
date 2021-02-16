---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409547"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет ту же функцию, что и функция [HrOpenABEntryWithProviderUID,](hropenabentrywithprovideruid.md) за исключением того, что функция **HrOpenABEntryWithProviderUIDSupport** открывает запись с использованием заданного объекта поддержки, а не сеанса и адресной книги. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Параметры

 _pEmsabpUID_
  
> [in] Указатель на параметр  _emsabpUID,_ который определяет поставщика адресной книги Exchange, который эта функция должна использовать для отображения сведений об идентификаторе записи. Если идентификатор входной записи не является идентификатором записи поставщика адресной книги Exchange, этот параметр игнорируется, и вызов функции действует точно так же, как [IAddrBook::D etails](iaddrbook-details.md). Если этот параметр имеет значение NULL или mapIUID нулевого уровня, эта функция также действует точно так же, как [IAddrBook::D etails.](iaddrbook-details.md)
    
 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса, который будет использоваться для доступа к открытой записи. Передача NULL возвращает стандартный интерфейс объекта. Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md). Для списков рассылки это [IDistList : IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров — [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Вызывающие могут установить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._ Можно установить следующие флаги: 
    
AB_TELL_DETAILS_CHANGE
  
> Указывает, что details возвращает true, если фактически в адрес были внесены изменения; в противном случае details возвращает false.
    
DIALOG_MODAL
  
> Отображает модальной версии диалоговое окно общего адреса. Этот флаг является взаимоисключающими с DIALOG_SDI.
    
DIALOG_SDI
  
> Отображает неавтомтную версию общего диалоговых окна адресов. Этот флаг является взаимоисключающими с DIALOG_MODAL.
    
MAPI_UNICODE
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _lpulObjType_
  
> [out] Указатель на тип открытой записи.
    
 _lppUnk_
  
> [out] Указатель на указатель открытой записи.
    

