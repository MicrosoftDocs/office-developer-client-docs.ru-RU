---
title: Метод SubmitChanges (RDS)
TOCTitle: SubmitChanges Method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 521728af91967d673a1c69f4e4812b0aaa73ce59
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883885"
---
# <a name="submitchanges-method-rds"></a>Метод SubmitChanges (RDS)


**Применимо к**: Access 2013, Office 2013

Отправляет ожидающие изменения локально кэширования и обновляемых [записей](recordset-object-ado.md) в источник данных, указанный в свойстве [Connect](connect-property-rds.md) или свойстве [URL-адрес](url-property-rds.md) .

## <a name="syntax"></a>Синтаксис

*DataControl*. SubmitChanges

*DataFactory*. SubmitChanges*подключения*, *записей*

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

  - *DataFactory*

  - Объектная переменная, которая представляет объект [RDSServer.DataFactory](datafactory-object-rdsserver.md) .

  - *Подключение*

  - Значение типа **String** , представляющий подключение, созданных с помощью **RDS. DataControl** **Подключить** свойства объекта.

  - *Набор записей*

  - Объектная переменная, представляющий объект **набора записей** .

## <a name="remarks"></a>Замечания

Необходимо задать свойства [подключения](connect-property-rds.md), [сервер](server-property-rds.md)и [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) , прежде чем использовать метод **SubmitChanges** с **RDS. DataControl** объекта.

При вызове метода [CancelUpdate](cancelupdate-method-rds.md) после вызова **SubmitChanges** для одного объекта **набора записей** , **CancelUpdate** завершается неудачно, так как эти изменения уже была выполнена.

Измененные записи будут отправлены для изменения и всех изменений выполнен удачно или все из них нет друг с другом.

**SubmitChanges** можно использовать только с помощью объекта **RDSServer.DataFactory** *по умолчанию* . Этот способ нельзя использовать настраиваемые бизнес-объекты.

Если свойство **URL-адрес** **SubmitChanges** будет внесения изменений в расположении, указанном URL-адрес.

