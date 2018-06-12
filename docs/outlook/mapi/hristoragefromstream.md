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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: bd2d0a662585e8aba91250786f88dd310fe37e32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808687"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Применимо к**: Outlook 
  
Слои интерфейс **IStorage** на объект **IStream** . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Parameters

 _lpUnkIn_
  
> [in] Указатель на **интерфейс IUnknown** объект, реализующий **IStream**. 
    
 _lpInterface_
  
> [in] Указатель на объект stream с идентификатором интерфейса (ИД интерфейса). Может быть передан в параметре _lpInterface_ , какие-либо из следующих значений: значение NULL, IID_IStream или IID_ILockBytes. Указать значение NULL для _lpInterface_ совпадает с передачей IID_IStream. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как должен быть создан относительно в потоке объекта хранилища. Значение по умолчанию — STGSTRM_RESET, который предоставляет доступ только для чтения объекта хранилища и запускает его в нулевой позиции потока. Следующие флаги могут устанавливаться в любом сочетании, за исключением как было указано:
    
STGSTRM_CREATE 
  
> Создает новый объект хранилища для объекта потока. Не удается установить этот флаг, если установлен флаг STGSTRM_RESET. 
    
STGSTRM_CURRENT 
  
> Запускает хранилища в текущей позиции потока. Не удается установить этот флаг, если установлен флаг STGSTRM_RESET. 
    
STGSTRM_MODIFY 
  
> Позволяет вызова поставщику услуг для записи возвращенные хранилища. Не удается установить этот флаг, если установлен флаг STGSTRM_RESET. 
    
STGSTRM_RESET 
  
> Запускает хранилища в нулевой позиции. Не удается установить этот флаг, если установить любой другой флаг. 
    
 _lppStorageOut_
  
> [out] Указатель на указатель на возвращенный объект **IStorage** . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Сообщение хранилища поставщики поддерживают функцию **HrIStorageFromStream** , с помощью интерфейса **IStorage** для вложений. Поставщики Store должна реализовать интерфейс **IStream** . **HrIStorageFromStream** предоставляет интерфейс **IStorage** для объекта **IStream** . Можно передать **ILockBytes** или интерфейс **IStream** в _lpUnkIn_. 
  

