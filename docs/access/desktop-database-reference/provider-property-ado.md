---
title: Свойство Provider (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df764aca267cab9b38760c432cd19154d6c6827f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881568"
---
# <a name="provider-property-ado"></a>Свойство Provider (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает имя поставщика для объекта [подключения](connection-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, указывающее имя поставщика.

## <a name="remarks"></a>Замечания

Используйте свойство **поставщика** или возвращает имя поставщика для подключения. Это свойство также можно установить с содержимое со значением свойства [ConnectionString](connectionstring-property-ado.md) или аргумент *ConnectionString* метода [Open](open-method-ado-connection.md) ; Тем не менее определение поставщика в нескольких местах, во время вызова метода **Open** может привести к непредсказуемым результатам. Если поставщик не указан, свойство по умолчанию MSDASQL ([Поставщик Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)).

Свойство **поставщика** — чтение и запись при подключении закрытой и только для чтения при открытии. Параметр вступает в силу до при открытии объект **подключения** или коллекции [свойств](properties-collection-ado.md) объекта **подключения** . Если параметр не является допустимым, возникает ошибка.

