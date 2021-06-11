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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Слой **интерфейса IStorage** на **объект IStream.** 
  
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

## <a name="parameters"></a>Parameters

 _lpUnkIn_
  
> [in] Указатель на **объект IUnknown,** реализующий **IStream.** 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для объекта потока. Любое из следующих значений можно передать в  _параметре lpInterface:_ NULL, IID_IStream или IID_ILockBytes. Передача NULL в  _lpInterface_ такая же, как передача IID_IStream. 
    
 _ulFlags_
  
> [in] Bitmask флагов, которые контролируют, как должен быть создан объект хранилища по отношению к потоку. Параметр по умолчанию STGSTRM_RESET, который предоставляет объекту хранилища только для чтения доступ и запускает его в нулевом положении потока. Следующие флаги можно установить в любой комбинации, за исключением отмеченных:
    
STGSTRM_CREATE 
  
> Создает новый объект хранения для объекта потока. Этот флаг нельзя установить, если STGSTRM_RESET заданной. 
    
STGSTRM_CURRENT 
  
> Запускает хранилище в текущем положении потока. Этот флаг нельзя установить, если STGSTRM_RESET заданной. 
    
STGSTRM_MODIFY 
  
> Позволяет поставщику вызываемой службы записывать на возвращенное хранилище. Этот флаг нельзя установить, если STGSTRM_RESET заданной. 
    
STGSTRM_RESET 
  
> Запускает хранилище с нулевой позиции. Этот флаг нельзя установить, если заданной является другой флаг. 
    
 _lppStorageOut_
  
> [вышел] Указатель на указатель на возвращенный **объект IStorage.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики магазинов сообщений поддерживают **функцию HrIStorageFromStream** с помощью **интерфейса IStorage** для вложений. Поставщики магазинов должны реализовать **интерфейс IStream.** **HrIStorageFromStream** предоставляет **интерфейс IStorage** для **объекта IStream.** В _lpUnkIn_ можно передать **интерфейс ILockBytes** или **IStream.** 
  

