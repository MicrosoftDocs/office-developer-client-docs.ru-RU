---
title: Свойство NativeError (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d572e7629deca0c7732bafbdfdb0c600ce34a35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880182"
---
# <a name="nativeerror-property-ado"></a>Свойство NativeError (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает код ошибки поставщика для того или иного объекта [ошибки](error-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** , указывающее код ошибки.

## <a name="remarks"></a>Замечания

Используйте свойство **NativeError** получение сведений о базе данных об ошибке для определенный объект **Error** . Например при использовании поставщика ODBC Microsoft для OLE DB с базой данных Microsoft SQL Server, коды собственной ошибки, которые создаются из SQL Server проходить через ODBC и поставщика ODBC свойство ADO **NativeError** .

