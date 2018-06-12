---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807138"
---
# <a name="calludf"></a>CallUDF

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Вызывает пользовательскую функцию в вычислительной среде высокой производительности.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parameters

_Код сеанса_
  
> Идентификатор сеанса, в котором для выполнения вызова.
    
_XLLName_
  
> Имя XLL, содержащий пользовательскую функцию.
    
_UDFName_
  
> Имя пользовательской функции.
    
_CallBackAddr_
  
> Функция, которая соединитель должен вызывать после завершения пользовательских функций.
    
_pxAsyncHandle_
  
> Асинхронный дескриптор, используемых в Excel и соединитель для отслеживания вызовов ожидающих пользовательских функций. Соединитель использует его более поздняя версия после завершения вызова, когда он вызывает Excel с помощью указатель функции передается в аргументе _CallBackAddr_ . 
    
_ArgCount_
  
> Число аргументов, передаваемых в пользовательской функции. Максимально допустимое значение — 255.
    
_Параметр1_
  
> Значение для передачи пользовательской функции. Повторите этот аргумент для каждого параметра, указанный в параметре _ArgCount_.
    
## <a name="return-value"></a>������������ ��������

**xlHpcRetSuccess** Если UDF успешно звонок; **xlHpcRetInvalidSessionId** Если недопустимый _SessionId_ аргумент; **xlHpcRetCallFailed** на другие сбои, включая время ожидания. Если звонок возвращает код ошибки (все, кроме **xlHpcRetSuccess**), затем Excel считает вызов пользовательских Функций, не были выполнены, признает недействительным _pxAsyncHandle_и не ожидает обратного вызова будет выполнена.
  
## <a name="remarks"></a>Замечания

Эта функция выполняет асинхронно.
  
## <a name="see-also"></a>См. также

- [Функции соединителя кластера Excel](excel-cluster-connector-functions.md)

