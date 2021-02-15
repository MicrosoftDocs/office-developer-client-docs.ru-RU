---
title: Свойство NativeError (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 86734d77cafd8dbe3c26219e291c16b81ef0026b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288612"
---
# <a name="nativeerror-property-ado"></a>Свойство NativeError (ADO)


**Область применения**: Access 2013, Office 2013

Указывает код ошибки конкретного поставщика для заданного [объекта Error.](error-object-ado.md)

## <a name="return-value"></a>Возвращаемое значение

Возвращает **длинное значение,** которое указывает код ошибки.

## <a name="remarks"></a>Заметки

Используйте свойство **NativeError** для получения сведений об ошибках для определенного объекта **Error.** Например, при использовании поставщика Microsoft ODBC для OLE DB с базой данных Microsoft SQL Server коды ошибок из SQL Server проходят через ODBC и поставщик ODBC в свойство ADO **NativeError.**

