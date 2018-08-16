---
title: Обработка ошибок в MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6f0ebd2112b65140a106a1376896f6de9c00da1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808390"
---
# <a name="error-handling-in-mapi"></a>Обработка ошибок в MAPI

**Относится к**: Outlook 
  
Успех, предупреждения и ошибки значения возвращаются с помощью 32-разрядное число, в результате известные дескриптор или HRESULT. HRESULT самом деле не маркер на что-либо; Это просто значение 32-разрядная версия с несколько полей в значения кодировке. Нулевой результат означает успешное выполнение и отличное от нуля результат указывает на ошибку.
  
MAPI на 32-разрядных платформах работает только с значения HRESULT.
  
На следующем рисунке показана формат HRESULT для 32-разрядных платформ.
  
**Формат HRESULT**
  
![Формат HRESULT] (media/amapi_49.gif "Формат HRESULT")
  
Старшего бита в значение HRESULT указывает тип возвращаемого значения: успешное или неудачное. Если значение 0, значение указывает на успешное завершение. Если задано значение 1, это означает сбой.
  
R, C, N и r бит зарезервированные в значение HRESULT.
  
Поле оборудование в обеих версиях указывает области ответственности для ошибки. Существует несколько средств, однако большинство ошибок MAPI использовать FACILITY_ITF для представления ошибки интерфейса. Наиболее распространенные производственные объекты, используемые в настоящее время являются: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC и FACILITY_STORAGE. При необходимости новые функции Microsoft выделяет их, так как они должны быть уникальными. В следующей таблице описаны различные поля оборудование.
  
|Оборудование|Описание|
|:-----|:-----|
|FACILITY_NULL  <br/> |Для широко применяемые основные коды состояния, таких как значение S_OK или E_OUTOF_MEMORY; значение равно нулю.  <br/> |
|FACILITY_ITF  <br/> |Для большинства коды состояния, возвращаемые из методов интерфейса; значение определяется с помощью интерфейса. То есть два значения HRESULT точно совпадает с 32-разрядная версия возвращаются из двух разных интерфейсов может иметь различные значения.  <br/> |
|FACILITY_DISPATCH  <br/> |Позднего связывания [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) интерфейса ошибки.  <br/> |
|FACILITY_RPC  <br/> |Для коды состояния, возвращаемые из удаленных вызовов процедур.  <br/> |
|FACILITY_STORAGE  <br/> |Для коды состояния, возвращаемые [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) или [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) вызовы методов, относящиеся к структурированного хранилища. Коды состояния кода (меньше 16 бит) значения в диапазоне Windows коды ошибок (то есть, не превышает 256) значение соответствующего ошибки Windows.  <br/> |
   
В поле Код — уникальный номер, назначенный для представления сообщение об ошибке или предупреждение.
  
