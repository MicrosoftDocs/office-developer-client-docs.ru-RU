---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: bf1a84a1f305580fc9d9085753ab7eb5c62b8aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808470"
---
# <a name="fnidle"></a>FNIDLE
 
**Применимо к**: Outlook 
  
Определяет простоя процедуры, которая простоя подсистемы MAPI периодически вызывает в соответствии с приоритетом. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Функция реализован:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
|Вызывается функция:  <br/> |MAPI  <br/> |
|Соответствующий тип указателя:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameters

 _lpvContext_
  
> [in] Указатель на блок памяти, что MAPI передается простоя подпрограммы каждый раз вызывает его. Такой указатель передается к ядру простоя MAPI с помощью параметра _pvIdleParam_ с [FtgRegisterIdleRoutine](ftgregisteridleroutine.md). Данные в блоке памяти может предоставить контекст для вызова простоя действия, например, какие объекта, или текущее состояние длительной операции.
    
## <a name="return-value"></a>������������ ��������

FALSE 
  
> Простоя процедуру с прототип **FNIDLE** всегда должен возвращать значение FALSE. 
    
## <a name="remarks"></a>Замечания

Определенных функций простоя подпрограммы определяется при помощи клиентского приложения или поставщика услуг. 
  
Клиента или поставщика необходимо ограничить время выполнения каждого состояния простоя подпрограммы. Каждого состояния следует выполнить минимальный объем обработки, обновить текущее состояние в данные контекста, который указывает _lpvContext_и вернуться к ядру простоя MAPI. 
  
Клиента или поставщика необходимо вызвать функцию MAPI [MAPIInitIdle](mapiinitidle.md) перед его можно регистрировать свой собственный простоя подпрограммы с вызова функции [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) . 
  
Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции FNIDLE простоя процедуры: 
  
|**Функция простоя процедуры**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменение характеристик зарегистрированных простоя процедуры.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированные простоя процедуру из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет простоя подпрограммы система MAPI, независимо от его включение.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Завершает работу обработчика бездействия MAPI для вызывающего приложения.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует обработчик простоя MAPI для вызывающего приложения.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**и **EnableIdleRoutine** принимают в качестве входного параметра, функция тег возвращаемых **FtgRegisterIdleRoutine**. 
  
При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению. Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет. 
  

