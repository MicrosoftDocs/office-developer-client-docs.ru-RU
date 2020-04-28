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


В этом разделе рассматриваются три типа поставщиков: поставщики данных, поставщики услуг и компоненты служб. Поставщики делятся на две категории: они предоставляют данные и предоставляют службы. *Поставщик данных* владеет собственными данными и предоставляет приложению доступ к нему в табличном виде. *Поставщик услуг* инкапсулирует службу, создавая и используя данные, расширяя функции в приложениях ADO. Поставщик услуг также может быть дополнительно определен как *компонент службы*, который должен работать совместно с другими поставщиками служб или компонентами.

## <a name="data-providers"></a>Поставщики данных

ADO является мощным и гибким, так как он может подключаться к любому из нескольких разных поставщиков данных и по-прежнему предоставлять одну и ту же модель программирования независимо от конкретных функций любого поставщика.

Тем не менее, так как каждый поставщик данных уникален, то, как приложение взаимодействует с ADO, немного зависит от поставщика данных. Различия обычно попадают в одну из трех категорий:

- Параметры подключения в свойстве [ConnectionString](connectionstring-property-ado.md) .

- Использование объекта [Command](command-object-ado.md) .

- Поведение [набора записей](recordset-object-ado.md) , зависящее от поставщика.

Подробные сведения о каждом из поставщиков данных, доступных в Майкрософт, перечислены ниже.

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
<td><p>Служба индексирования (Майкрософт)</p></td>
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
<td><p>Публикация в Интернете</p></td>
<td><p><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a>Динамические свойства, зависящие от поставщика

Коллекции [свойств](properties-collection-ado.md) объекта [подключения](connection-object-ado.md), [команды](command-object-ado.md)и объекта [Recordset](recordset-object-ado.md) содержат динамические свойства, характерные для поставщика. Эти свойства предоставляют сведения о функциях, относящихся к поставщику, за пределами встроенных свойств, поддерживаемых ADO.

После установки подключения и создания этих объектов используйте метод [Refresh](refresh-method-ado.md) в коллекции **свойств** объекта, чтобы получить свойства, зависящие от поставщика. Для получения подробных сведений об этих динамических свойствах обратитесь к документации по поставщику и Справочнику программиста OLE DB.

## <a name="service-providers"></a>Поставщики служб

Для использования поставщика услуг необходимо указать ключевое слово. Кроме того, следует помнить о динамических свойствах, связанных с поставщиками, которые связаны с каждым поставщиком услуг. Сведения, относящиеся к поставщику, указаны для каждого из поставщиков услуг, доступных в корпорации Майкрософт:

- [Служба формирования данных (Майкрософт) для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [Поставщик службы сохранения Microsoft OLE DB](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [Поставщик удаленного взаимодействия OLE DB (Майкрософт)](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a>Компоненты служб

Компонент службы [курсора для службы OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) дополняют функциональные возможности поставщиков данных поддержки курсора. Кроме того, требуется ключевое слово и динамическое свойство.

Для получения дополнительных сведений о поставщиках обратитесь к документации Microsoft OLE DB в пакете SDK компонентов Microsoft Data Access или посетите [Центр разработчиков платформы данных](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).

## <a name="provider-commands"></a>Команды поставщика

Для каждого поставщика, указанного здесь, если ваши приложения позволяют пользователям вводить инструкции SQL в качестве команд поставщика, необходимо всегда проверять данные, введенные пользователем, и вигилант возможных атак хакеров, используя потенциально опасные инструкции SQL, например, как часть вводимых пользователем данных.

