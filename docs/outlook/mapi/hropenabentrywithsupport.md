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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Не используйте эту функцию.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |абхелп. h  <br/> |
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

## <a name="parameters"></a>Параметры

 _лпсуп_
  
> 
    
 _кбентрид_
  
> возврата Количество байт в идентификаторе записи, заданном параметром _лпентрид_ . 
    
 _лпентрид_
  
> возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.
    
 _лпинтерфаце_
  
>  возврата Указатель на идентификатор интерфейса (IID) интерфейса, который будет использоваться для доступа к открытой записи. При передаче значения NULL возвращается стандартный интерфейс объекта. Для пользователей обмена сообщениями стандартный интерфейс — [имаилусер: IMAPIProp](imailuserimapiprop.md). Для списков рассылки это [идистлист: IMAPIContainer](idistlistimapicontainer.md), а для контейнеров — [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md). Вызывающие абоненты могут установить _лпинтерфаце_ в соответствии со стандартным интерфейсом или интерфейсом в иерархии наследования. 
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющая тип текста для параметра _лпсзбуттонтекст_ . Можно задать следующие флаги: 
    
AB_TELL_DETAILS_CHANGE
  
> Указывает, что Details возвращает TRUE, если изменения фактически вносятся в адрес; в противном случае сведения возвращает значение FALSE.
    
DIALOG_MODAL
  
> Отображает модальную версию диалогового окна Общий адрес. Этот флаг является взаимно исключающим с DIALOG_SDI.
    
DIALOG_SDI
  
> Отображает немодальную версию диалогового окна общего адреса. Этот флаг является взаимно исключающим с DIALOG_MODAL.
    
MAPI_UNICODE
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.
    
 _лпулобжтипе_
  
> вышли Указатель на тип открытого элемента.
    
 _лппунк_
  
> вышли Указатель на указатель открытого элемента.
    

