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

Указывает, к [каков объект Connection,](connection-object-ado.md) к которому в настоящее время принадлежит указанный [объект Command,](command-object-ado.md) [Recordset](recordset-object-ado.md)или [Record.](record-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строку,** содержащую определение подключения, если подключение закрыто, или **вариант,** содержащий текущий объект **Connection,** если подключение открыто. Значение по умолчанию — это ссылка на объект null. См. [свойство ConnectionString.](connectionstring-property-ado.md)

## <a name="remarks"></a>Заметки

Используйте свойство **ActiveConnection,** чтобы определить объект **Connection,** для которого будет выполняться указанный **объект Command** или будет открыт указанный объект **Recordset.**

### <a name="command"></a>Команда

Для **объектов Command** свойство **ActiveConnection** имеет свойство read/write.

При попытке вызвать метод [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) для объекта **Command** перед установкой для этого свойства открытого объекта **Connection** или допустимой строки подключения возникает ошибка.

**Microsoft Visual Basic:** установка для свойства **ActiveConnection** свойства *Nothing* отключает связь объекта **Command** с текущим **подключением** и заставляет поставщика освободить все связанные ресурсы в источнике данных. Затем можно связать объект **Command** с тем же или другим объектом **Connection.** Некоторые поставщики позволяют изменить параметр свойства  с одного подключения на другой, не устанавливая для свойства *ничего.*

Если коллекция [Parameters](parameters-collection-ado.md) объекта **Command** содержит параметры, предоставленные поставщиком, коллекция очищается, если для свойства **ActiveConnection** установлено свойство *Nothing* или другой объект **Connection.** Если вы вручную создаете [объекты Parameter](parameter-object-ado.md) и используете их для заполнения коллекции Parameters объекта **Command,** установка для свойства **ActiveConnection** свойства *Nothing* или другого объекта **Connection** оставляет коллекцию **Parameters** без изменений. 

Закрытие объекта **Connection,** с которым связан **объект Command,** задает для **свойства ActiveConnection** свойство *Nothing.* При установке этого свойства на **закрытый объект Connection** создается ошибка.

### <a name="recordset"></a>Recordset

Для **открытых объектов Recordset** или **объектов Recordset,** свойство [Source](source-property-ado-recordset.md) которых имеет допустимый объект **Command,** свойство **ActiveConnection** имеет только чтение. В противном случае это чтение и написание.

Можно установить для этого свойства допустимый объект **Connection** или допустимую строку подключения. В этом случае поставщик создает новый объект **Connection** с помощью этого определения и открывает подключение. Кроме того, поставщик может установить для этого свойства новый объект **Connection,** чтобы предоставить доступ к объекту **Connection** для получения расширенных сведений об ошибке или выполнения других команд.

Если для открытия объекта **Recordset** используется аргумент *ActiveConnection* метода [Open,](open-method-ado-recordset.md) свойство **ActiveConnection** наследует значение аргумента.

Если для свойства  **Source** объекта **Recordset** установлена допустимая переменная объекта **Command,** свойство **ActiveConnection** объекта **Recordset** наследует параметр свойства **ActiveConnection** объекта Command.

Использование удаленной службы данных **:** при использовании в клиентском объекте Recordset это свойство может быть установлено только в строке подключения или (в Microsoft Visual Basic или Visual Basic, Scripting Edition) в *nothing*.

### <a name="record"></a>Record

Это свойство считывать и записывать при закрытии объекта **Record** и может содержать строку подключения или ссылку на **открытый объект Connection.** Это свойство только для чтения, когда открыт объект **Record,** и содержит ссылку на открытый **объект Connection.**

Объект **Connection** создается неявно, когда объект **Record** открывается из URL-адреса. Откройте запись **с** помощью существующего открытого объекта **Connection,** назначив этому свойству объект **Connection** или используя объект **Connection** в качестве параметра в вызове метода [Open.](open-method-ado-record.md) Если запись  **открывается** из существующего объекта **Record** или [Recordset,](recordset-object-ado.md)она автоматически связана с объектом Connection этого объекта Record или **Recordset.** 

> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)



