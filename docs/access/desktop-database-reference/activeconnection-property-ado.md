---
title: Свойство ActiveConnection (ADO)
TOCTitle: ActiveConnection property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 10/17/2018
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 037ae753f427c42f147972170dbb2e645b260623
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282532"
---
# <a name="activeconnection-property-ado"></a>Свойство ActiveConnection (ADO)

**Область применения**: Access 2013, Office 2013

Указывает, к какому объекту [подключения](connection-object-ado.md) принадлежит указанная [команда](command-object-ado.md), [набор записей](recordset-object-ado.md)или объект [Record](record-object-ado.md) , который в настоящее время принадлежит.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, содержащее определение подключения, если соединение закрыто, или **переменная Variant** , содержащая текущий объект **Connection** , если подключение открыто. Значение по умолчанию — пустая ссылка на объект. Просмотрите свойство [ConnectionString](connectionstring-property-ado.md) .

## <a name="remarks"></a>Замечания

Используйте свойство **ActiveConnection** для определения объекта **подключения** , для которого будет выполняться указанный объект **команды** , или будет открыт указанный **набор записей** .

### <a name="command"></a>Command

Для объектов **Command** свойство **ActiveConnection** доступно для чтения и записи.

Если вы попытаетесь вызвать метод [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) для объекта **Command** перед тем, как присвоить этому свойству объект открытого **подключения** или допустимую строку подключения, возникнет ошибка.

**Microsoft Visual Basic**: Установка для свойства **ActiveConnection** значения *Nothing* отменяет связь объекта **Command** с текущим **подключением** и заставляет поставщика освобождать все связанные ресурсы в данных. Source. Затем вы можете связать объект **Command** с тем же или другим объектом **Connection** . Некоторые поставщики позволяют изменить значение свойства с одного **подключения** на другое без необходимости устанавливать для свойства *значение Nothing*.

Если коллекция [Parameters](parameters-collection-ado.md) объекта **Command** содержит параметры, предоставляемые поставщиком, то коллекция очищается, если для свойства **ActiveConnection** задано значение *Nothing* или другое объект **Connection** . Если вы вручную создаете объекты [параметров](parameter-object-ado.md) и используете их для заполнения коллекции **Parameters** объекта **Command** , установка для свойства **ActiveConnection** значения *Nothing* или другого объекта **подключения** оставляет Коллекция **Parameters** не изменяется.

При закрытии объекта **подключения** , с которым связан объект **Command** , свойству **ActiveConnection** присваивается *значение Nothing*. При задании этого свойства для закрытого объекта **подключения** возникнет ошибка.

### <a name="recordset"></a>Recordset

Для объектов Open **Recordset** или объектов **Recordset** , свойству [Source](source-property-ado-recordset.md) которых присвоено значение допустимого объекта **Command** , свойство **ActiveConnection** доступно только для чтения. В противном случае он доступен для чтения и записи.

Этому свойству можно присвоить допустимый объект **подключения** или допустимую строку подключения. В этом случае поставщик создает новый объект **Connection** с помощью этого определения и открывает подключение. Кроме того, поставщик может задать для этого свойства новый объект **Connection** , чтобы предоставить доступ к объекту **Connection** для расширенных сведений об ошибках или выполнить другие команды.

Если вы используете аргумент *ActiveConnection* метода [Open](open-method-ado-recordset.md) , чтобы открыть объект **Recordset** , свойство **ActiveConnection** унаследует значение аргумента.

Если присвоить свойству **Source** объекта **Recordset** допустимую переменную объект **Command** , свойство **ActiveConnection** объекта **Recordset** наследует параметр **** ** Свойство ActiveConnection** .

**Использование удаленной службы данных**: при использовании в объекте Recordset на стороне клиента это свойство можно задать только для строки подключения или (в Microsoft Visual Basic или Visual Basic, Scripting Edition) на *Nothing*.

### <a name="record"></a>Record

Это свойство доступно для чтения и записи, когда объект **Record** закрыт, и может содержать строку подключения или ссылку на открытый объект **подключения** . Это свойство доступно только для чтения, если открыт объект **Record** , и содержит ссылку на объект открытого **подключения** .

Объект **Connection** неявно создается при открытии объекта **Record** по URL-адресу. Откройте **запись** с существующим объектом открытого **подключения** , назначив объект **Connection** этому свойству или используя объект **Connection** в качестве параметра в вызове метода [Open](open-method-ado-record.md) . Если **запись** открыта из существующей **записи** или [набора записей](recordset-object-ado.md), она автоматически связывается с этой записью **** или объектом **подключения** объекта **Recordset** .

> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически будут вызывать [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [абсолютные и относительНые URL-адреса](absolute-and-relative-urls.md).



