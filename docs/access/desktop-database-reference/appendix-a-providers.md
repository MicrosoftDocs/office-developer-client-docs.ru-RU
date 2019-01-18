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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717054"
---
# <a name="appendix-a-providers"></a>Приложение А. Поставщики


**Применимо к**: Access 2013, Office 2013


В данном разделе описываются три вида поставщиков: поставщики данных, поставщиков услуг и компоненты службы. Поставщики могут быть разделены на две категории: те, предоставляя данные и те, обеспечивающих работу служб. *Поставщик данных* несет ответственность за свои собственные данные и предоставляет доступ к нему в виде таблицы в приложение. *Поставщик услуг* инкапсулирует службы путем создания и использования данных, дополнения функции в приложениях ADO. Поставщик службы может также быть разбить как *компонент службы*, которым необходимо работать совместно с другими поставщиками услуг или компоненты.

## <a name="data-providers"></a>Поставщики данных

ADO мощные и гибкие, так как он может подключиться к любой из нескольких разных поставщиков данных и по-прежнему предоставляют доступ к той же модели программирования, вне зависимости от конкретных компонентов любого заданного поставщика.

Тем не менее так как каждый поставщик данных является уникальным, как приложение взаимодействует с ADO будет отличаться поставщиком данных. Различия обычно делятся на три категории.

- Параметры подключения в свойстве [ConnectionString](connectionstring-property-ado.md) .

- Использование объекта [команды](command-object-ado.md) .

- Поставщик поведение [набора записей](recordset-object-ado.md) .

Подробные сведения для каждого из поставщиков данных, доступные в настоящее время корпорацией Майкрософт перечислены ниже.

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
<td><p><a href="microsoft-ole-db-provider-for-odbc.md">Поставщик Microsoft OLE DB для ODBC</a></p></td>
</tr>
<tr class="even">
<td><p>Служба индексирования</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Поставщик Microsoft OLE DB для службы индексирования (Майкрософт)</a></p></td>
</tr>
<tr class="odd">
<td><p>Службы Microsoft Active Directory</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Поставщик Microsoft OLE DB для службы Microsoft Active Directory</a></p></td>
</tr>
<tr class="even">
<td><p>Базы данных Microsoft Jet</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Поставщик Microsoft OLE DB для Microsoft Jet</a></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft SQL Server</p></td>
<td><p><a href="microsoft-ole-db-provider-for-sql-server.md">Поставщик Microsoft OLE DB для SQL Server</a></p></td>
</tr>
<tr class="even">
<td><p>Базы данных Oracle</p></td>
<td><p><a href="microsoft-ole-db-provider-for-oracle.md">Поставщик Microsoft OLE DB для Oracle</a></p></td>
</tr>
<tr class="odd">
<td><p>Публикации в Интернете</p></td>
<td><p><a href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации в Интернете</a></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a>Динамические свойства от поставщика

Коллекции [свойств](properties-collection-ado.md) объектов [подключения](connection-object-ado.md), [команды](command-object-ado.md)и [набора записей](recordset-object-ado.md) включают динамических свойств, относящихся к поставщику. Эти свойства предоставляют информацию о функциональные возможности к поставщику за пределы встроенных свойств, которые поддерживает ADO.

После подключения к и создания этих объектов, используйте метод [Refresh](refresh-method-ado.md) в коллекции **свойств** объекта для получения свойства от поставщика. Обратитесь к документации поставщика и Справочник программиста OLE DB для получения дополнительных сведений об этих динамических свойств.

## <a name="service-providers"></a>Поставщики служб

Чтобы использовать поставщика услуг, необходимо указать ключевое слово. Кроме того, необходимо принять во внимание от поставщика динамические свойства, связанные с каждой поставщика услуг. Сведения от поставщика, приведены для каждого из поставщиков услуг, доступные в настоящее время корпорации Майкрософт:

- [Microsoft службы формирования данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [Сохраняемость поставщик Microsoft OLE DB](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [Поставщик Microsoft OLE DB удаленного доступа](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a>Компоненты службы

Компонент службы [Служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) дополняет функции поддержки курсора поставщиков данных. Он также требует использования ключевого слова и имеет динамические свойства.

Дополнительные сведения о поставщиках обратитесь к документации по Microsoft OLE DB в пакете SDK компонентов доступа к данным Microsoft или посетите [Центр разработчиков данных платформы](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).

## <a name="provider-commands"></a>Команды поставщика

Для каждого поставщика в списке, если ваши приложения позволяют пользователям вводить инструкции SQL как команды поставщика, необходимо всегда вводимых пользователем и быть бдительность возможные злоумышленник атак с помощью потенциально опасных инструкции SQL, например, как часть Ввод данных пользователем.

