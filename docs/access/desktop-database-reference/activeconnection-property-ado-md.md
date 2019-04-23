---
title: Свойство ActiveConnection (ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 372dac11500647af75881ae6b4aee22a391a32c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280531"
---
# <a name="activeconnection-property-ado-md"></a>Свойство ActiveConnection (ADO MD)

**Область применения**: Access 2013, Office 2013

Указывает, какой объект [подключения](connection-object-ado.md) ADO принадлежит текущему набору ячеек или каталогу в текущий момент.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **значение Variant** , содержащее строку, определяющую подключение или объект **Connection** . Значение по умолчанию — пустое значение.

## <a name="remarks"></a>Замечания

Этому свойству можно присвоить допустимый объект **подключения** ADO или допустимую строку подключения. Если для этого свойства задано значение строка подключения, поставщик создает новый объект **Connection** с помощью этого определения и открывает подключение.

Если для открытия объекта [Cell](cellset-object-ado-md.md) используется аргумент **ActiveConnection** метода [Open](open-method-ado-md.md) , свойство **ActiveConnection** наследует значение аргумента.

Установка для свойства **ActiveConnection** объекта [каталога](catalog-object-ado-md.md) значения **Nothing** приводит к освобождению связанных данных, в том числе данных в коллекции [коллекция cubedefs](cubedefs-collection-ado-md.md) , а также любых связанных [измерений](dimension-object-ado-md.md), [иерархий](hierarchy-object-ado-md.md), [уровней](level-object-ado-md.md) и объекты [member](member-object-ado-md.md) . Закрытие объекта **подключения** , который использовался для открытия **каталога** , имеет тот же результат, что и установка для свойства **ActiveConnection** значения **Nothing**.

Изменение базы данных по умолчанию для подключения, указанного в свойстве **ActiveConnection** объекта **Catalog** , делает содержимое **каталога**недействительным.

Если вы попытаетесь изменить свойство **ActiveConnection** для открытого объекта "набор **ячеек** ", произойдет ошибка.

> [!NOTE]
> В Visual Basic не забывайте использовать ключевое слово **Set** при задании свойства **ActiveConnection** для объекта **Connection** . Если опустить ключевое слово **Set** , в действительности будет задано свойство **ActiveConnection** , равное свойству по умолчанию объекта **подключения** , **ConnectionString**. Код будет работать; Однако вы создадите дополнительное подключение к источнику данных, что может негативно сказаться на производительности.

При использовании поставщика данных MSOLAP присвойте источнику данных в строке подключения имя сервера и присвойте начальному каталогу имя каталога из источника данных. Чтобы подключиться к файлу куба, который отключен от сервера, укажите в качестве расположения полный путь к файлу. Файл CUB. В любом случае задайте поставщику имя поставщика. Например, следующая строка подключается к каталогу с именем Бобс Video Store на сервере с именем ServerName и поставщиком MSOLAP:

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

Следующая строка подключается к файлу локального куба в каталоге C\\: мсдасдк\\Samples\\OLEDB\\\\Data\\бобсвид. cub:

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

