---
title: Приложение А. Поставщики
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4549c8817361cfb5b9fa730ee37ca6a07edc98b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297062"
---
# <a name="appendix-a-providers"></a>Приложение А. Поставщики


**Область применения**: Access 2013, Office 2013


Этот раздел посвящен трем типам поставщиков: поставщикам данных, поставщикам услуг и компонентам служб. Поставщики подпадают под две категории: поставщики, предоставляющие данные, и поставщики услуг. Поставщик *данных владеет* собственными данными и предоставляет их приложению в табличной форме. Поставщик услуг инкапсулирует службу, выдав и потребляя данные, дополнив функции в приложениях ADO.  Поставщик услуг также может быть далее определен как компонент *службы,* который должен работать в сочетании с другими поставщиками или компонентами службы.

## <a name="data-providers"></a>Поставщики данных

ADO — это мощный и гибкий инструмент, так как он может подключаться к любому из разных поставщиков данных и по-прежнему использовать ту же модель программирования независимо от конкретных функций конкретного поставщика.

Однако, так как каждый поставщик данных уникален, способ взаимодействия приложения с ADO немного зависит от поставщика данных. Различия обычно подпадают под одну из трех категорий:

- Параметры подключения в [свойстве ConnectionString.](connectionstring-property-ado.md)

- [Использование объекта](command-object-ado.md) command.

- Поведение наборов [записей для конкретного](recordset-object-ado.md) поставщика.

Ниже перечислены сведения о каждом поставщике данных, доступных в настоящее время корпорацией Майкрософт.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Область</p></th>
<th><p>Тема</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Базы данных ODBC</p></td>
<td><p><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></p></td>
</tr>
<tr class="even">
<td><p>Служба индексации (Майкрософт)</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></p></td>
</tr>
<tr class="odd">
<td><p>Служба Microsoft Active Directory</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></p></td>
</tr>
<tr class="even">
<td><p>Базы данных Microsoft Jet</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft SQL Server</p></td>
<td><p><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></p></td>
</tr>
<tr class="even">
<td><p>Базы данных Oracle</p></td>
<td><p><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></p></td>
</tr>
<tr class="odd">
<td><p>Интернет-публикация</p></td>
<td><p><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a>Динамические свойства для конкретного поставщика

Коллекции [свойств объектов](properties-collection-ado.md) [Connection,](connection-object-ado.md) [Command](command-object-ado.md)и [Recordset](recordset-object-ado.md) включают динамические свойства, специфические для поставщика. Эти свойства предоставляют сведения о функциях, характерных для поставщика, помимо встроенных свойств, поддерживаемых ADO.

После установления подключения и создания этих объектов используйте метод [Refresh](refresh-method-ado.md) в коллекции **свойств** объекта для получения свойств, характерных для конкретного поставщика. Подробные сведения об этих динамических свойствах можно найти в документации поставщика и справочнике программиста OLE DB.

## <a name="service-providers"></a>Поставщики служб

Чтобы использовать поставщика услуг, необходимо предоставить ключевое слово. Также следует знать о динамических свойствах, связанных с каждым поставщиком услуг. Сведения о поставщике перечислены для каждого поставщика услуг, доступных в настоящее время корпорацией Майкрософт:

- [Служба формирования данных Майкрософт для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [Поставщик сохраняемости Microsoft OLE DB](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [Microsoft OLE DB Remoting Provider](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a>Компоненты службы

Компонент [службы курсора для службы OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) дополняет курсор поддержки функций поставщиков данных. Кроме того, для него требуется ключевое слово и динамические свойства.

Дополнительные сведения о поставщиках см. в документации по Microsoft OLE DB в microsoft Data Access Components SDK или в Центре разработчиков [платформы данных.](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)

## <a name="provider-commands"></a>Команды поставщика

Если приложения позволяют пользователям вводить операторы SQL в качестве команд поставщика для каждого из перечисленных здесь поставщиков, необходимо всегда проверять входные данные пользователей и быть внимательными к возможным атакам хакеров с помощью потенциально опасных операторов SQL, например, в составе пользовательского ввода.

