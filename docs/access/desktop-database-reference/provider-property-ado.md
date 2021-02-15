---
title: Свойство Provider (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e640fb6131919cbdf88fbbf8229c62d0e2e4e13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301136"
---
# <a name="provider-property-ado"></a>Свойство Provider (ADO)


**Область применения**: Access 2013, Office 2013

Указывает имя поставщика для объекта [Connection.](connection-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строку,** которая указывает имя поставщика.

## <a name="remarks"></a>Заметки

Используйте свойство **Provider,** чтобы установить или вернуть имя поставщика для подключения. Это свойство также можно установить с помощью содержимого свойства [ConnectionString](connectionstring-property-ado.md) или *аргумента ConnectionString* метода [Open;](open-method-ado-connection.md) Однако указание поставщика в более чем одном месте при вызове метода **Open** может привести к непредсказуемым результатам. Если поставщик не указан, свойство по умолчанию имеет значение MSDASQL[(Поставщик Microsoft OLE DB для ODBC).](microsoft-ole-db-provider-for-odbc.md)

Свойство **Provider** считывать и записывать при закрытии подключения и только для чтения, когда оно открыто. Параметр не вступает в силу, пока вы не откроете объект **Connection** или не откроете коллекцию [свойств](properties-collection-ado.md) объекта **Connection.** Если этот параметр не является допустимым, возникает ошибка.

