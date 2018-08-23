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
ms.openlocfilehash: d6f5a0bd5da851c5107b8d3d40d683a7e3c1b26b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586013"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Выполняет те же функции, что функцию [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) , за исключением того, что функция **HrOpenABEntryWithProviderUIDSupport** открывает запись, с помощью объекта заданного поддержки вместо использования сеанса и адресной книги. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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
  
> [in] Указатель на параметр _emsabpUID_ , который определяет поставщик адресной книги Exchange, который следует использовать эту функцию для отображения сведений на идентификатор записи. Если входящий идентификатор записи не идентификатор записи адресной книги Exchange поставщика, этот параметр игнорируется и действует вызова функции аналогично [IAddrBook::Details](iaddrbook-details.md). Если этот параметр имеет значение NULL или ноль MAPIUID, эта функция также работает так же, как [IAddrBook::Details](iaddrbook-details.md).
    
 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.
    
 _lpInterface_
  
> [in] Указатель на интерфейс идентификатор (ИД интерфейса) интерфейс, который будет использоваться для доступа к открытой операцией. Передача NULL Возвращает стандартный интерфейс объекта. Для пользователей, обмена мгновенными сообщениями, — это стандартный интерфейс [IMailUser: IMAPIProp](imailuserimapiprop.md). Для списков рассылки, он является [IDistList: IMAPIContainer](idistlistimapicontainer.md)и для контейнеров, это [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Вызывающие объекты можно задать _lpInterface_ соответствующий стандартный интерфейс или интерфейс в иерархии наследования. 
    
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
    
 _lpulObjType_
  
> [out] Указатель на тип открыт записи.
    
 _lppUnk_
  
> [out] Указатель на указатель открыт записи.
    

