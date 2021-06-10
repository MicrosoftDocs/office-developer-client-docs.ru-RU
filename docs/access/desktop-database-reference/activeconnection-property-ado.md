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

Указывает, к каков [объекту Подключение,](connection-object-ado.md) которому в настоящее время принадлежит [объект Command,](command-object-ado.md) [Recordset](recordset-object-ado.md)или [Record.](record-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **String,** содержащее определение подключения, если подключение  закрыто, или Вариант, содержащий текущий объект **Подключения,** если подключение открыто. По умолчанию — это ссылка на объект null. См. свойство [ConnectionString.](connectionstring-property-ado.md)

## <a name="remarks"></a>Примечания

Используйте свойство **ActiveConnection** для определения объекта **Подключения,** над которым будет выполняться указанный объект **Command** или будет открыт указанный **набор** записей.

### <a name="command"></a>Команда

Для **объектов Command** свойство **ActiveConnection** считыванию или записи.

При попытке вызвать метод [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) на **объекте Command** перед  установкой этого свойства на открытый объект подключения или допустимую строку подключения возникает ошибка.

**Microsoft Visual Basic:** Настройка свойства **ActiveConnection** в *Nothing* отсоединяет объект  **Command** от текущего подключения и заставляет поставщика выпускать все связанные ресурсы в источнике данных. Затем можно связать объект **Command** с тем же или другим объектом **Подключения.** Некоторые поставщики позволяют изменять параметр свойства  с одного подключения на другое, не заявив сначала свойство *Nothing*.

Если коллекция [Параметры](parameters-collection-ado.md) объекта **Command** содержит параметры, предоставленные поставщиком, коллекция очищается, если вы задаете свойство **ActiveConnection** объекту *Nothing* или другому объекту **Подключения.** Если вы вручную создаете [объекты Параметры](parameter-object-ado.md) и используете их для заполнения коллекции  Параметры объекта   **Command,**  параметры свойства **ActiveConnection** не будут повреждены.

Закрытие объекта **Подключения,** с которым связан **объект Command,** задает свойство **ActiveConnection** *nothing*. Настройка этого свойства для закрытого объекта **Подключения** создает ошибку.

### <a name="recordset"></a>Recordset

Для **открытых объектов Recordset** или объектов **Recordset,** для которых свойство [Source](source-property-ado-recordset.md) установлено для допустимого объекта **Command,** свойство **ActiveConnection** является только для чтения. В противном случае это чтение или написание.

Это свойство можно настроить на допустимый **объект Подключения** или допустимую строку подключения. В этом случае поставщик создает новый объект **Подключения** с помощью этого определения и открывает подключение. Кроме того, поставщик может настроить это свойство для нового объекта **Подключения,** чтобы предоставить доступ к объекту **Connection** для получения расширенных сведений об ошибках или выполнения других команд.

Если для открытия объекта **Recordset** используется аргумент *ActiveConnection* метода [Open,](open-method-ado-recordset.md) свойство **ActiveConnection** наследует значение аргумента.

Если вы  установите свойство Source объекта **Recordset** допустимой переменной объекта Command, свойство **ActiveConnection** в  **Recordset** наследует параметр свойства **ActiveConnection** объекта Command. 

**Удаленное** использование службы данных. При использовании на клиентском объекте Recordset это свойство можно установить только в строке подключения или (в Microsoft Visual Basic или Visual Basic, Scripting Edition) в *Nothing*.

### <a name="record"></a>Record

Это свойство читается или записи, когда объект **Record** закрыт, и может содержать строку подключения или ссылку на открытый объект **Подключения.** Это свойство только для чтения, когда объект **Record** открыт, и содержит ссылку на открытый объект **Подключения.**

Объект **Подключения** создается неявно, когда объект **Record** открывается с URL-адреса. Откройте запись **с** помощью существующего открытого объекта **Подключения,** назначив этому свойству объект **Connection** или используя объект **Connection** в качестве параметра в вызове [метода Open.](open-method-ado-record.md) Если запись **открыта** из существующего объекта  **Record** или [Recordset,](recordset-object-ado.md)  она автоматически связана с объектом Подключения этого объекта Record или **Recordset.**

> [!NOTE]
> URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)



