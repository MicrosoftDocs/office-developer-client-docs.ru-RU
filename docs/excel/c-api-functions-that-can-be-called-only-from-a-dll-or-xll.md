---
title: Функции интерфейса API для C, которые могут вызываться только из DLL или XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции [excel 2007], c api вызов выполняется из dll или xll
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807151"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>Функции интерфейса API для C, которые могут вызываться только из DLL или XLL

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
API-Интерфейс C предоставляет 15 функции обратного вызова Microsoft Excel, которые могут вызываться только с помощью **Excel4**, **Excel4v**, **Excel12**или **Excel12v** функции (или один из этих функций, косвенно с помощью функции Framework **Excel **или **Excel12f**). Это означает, что они могут вызываться только из DLL или XLL.
  
## <a name="in-this-section"></a>В этом разделе

[xlAbort](xlabort.md)
  
[xlAsyncReturn](xlasyncreturn.md)
  
[xlCoerce](xlcoerce.md)
  
[xlDefineBinaryName](xldefinebinaryname.md)
  
[xlDisableXLMsgs](xldisablexlmsgs.md)
  
[xlEnableXLMsgs](xlenablexlmsgs.md)
  
[xlEventRegister](xleventregister.md)
  
[xlFree](xlfree.md)
  
[xlGetBinaryName](xlgetbinaryname.md)
  
[xlGetHwnd](xlgethwnd.md)
  
[xlGetInst](xlgetinst.md)
  
[xlGetInstPtr](xlgetinstptr.md)
  
[xlGetName](xlgetname.md)
  
[xlRunningOnCluster](xlrunningoncluster.md)
  
[функция xlSet](xlset.md)
  
[xlSheetId](xlsheetid.md)
  
[xlSheetNm](xlsheetnm.md)
  
[xlStack](xlstack.md)
  
[xlUDF](xludf.md)
  
## <a name="see-also"></a>См. также



[������� ��������� ������ API C Excel4 Excel12](c-api-callback-functions-excel4-excel12.md)

