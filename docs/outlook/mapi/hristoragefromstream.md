---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416834"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Слой **интерфейса IStorage** на объект **IStream.** 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Параметры

 _lpUnkIn_
  
> [in] Указатель на объект **IUnknown,** реализующий **IStream.** 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для объекта stream. В параметре  _lpInterface_ можно передать любое из следующих значений: NULL, IID_IStream или IID_ILockBytes. Передача NULL в  _lpInterface_ это то же, что передача IID_IStream. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет тем, как создается объект хранилища относительно потока. Значение по умолчанию — STGSTRM_RESET, который предоставляет объекту хранилища доступ только для чтения и запускает его с нуля в потоке. Следующие флаги можно установить в любом сочетании, кроме как отмечено:
    
STGSTRM_CREATE 
  
> Создает объект хранилища для объекта stream. Этот флаг нельзя установить, если STGSTRM_RESET установлен. 
    
STGSTRM_CURRENT 
  
> Запускает хранилище в текущем положении потока. Этот флаг нельзя установить, если STGSTRM_RESET установлен. 
    
STGSTRM_MODIFY 
  
> Позволяет поставщику услуг звонков записывать в возвращенное хранилище. Этот флаг нельзя установить, если STGSTRM_RESET установлен. 
    
STGSTRM_RESET 
  
> Запускает хранилище с нуля. Этот флаг нельзя установить, если установлен какой-либо другой флаг. 
    
 _lppStorageOut_
  
> [out] Указатель на указатель на возвращенный **объект IStorage.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики store сообщений поддерживают **функцию HrIStorageFromStream** с помощью **интерфейса IStorage** для вложений. Поставщики магазина должны реализовать **интерфейс IStream.** **HrIStorageFromStream** предоставляет **интерфейс IStorage** для **объекта IStream.** В _lpUnkIn_ можно передать **интерфейс ILockBytes** или **IStream.** 
  

