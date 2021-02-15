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

Указывает, к каков объекту подключения [ADO](connection-object-ado.md) текущий ячейки или каталог в настоящее время принадлежит.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **вариант,** содержащий строку, определяя подключение или **объект Connection.** Значение по умолчанию пустое.

## <a name="remarks"></a>Заметки

Вы можете установить для этого свойства допустимый объект подключения **ADO** или допустимую строку подключения. Если для этого свойства установлена строка подключения, поставщик создает новый объект **Connection** с помощью этого определения и открывает подключение.

Если для открытия объекта [Cellset](cellset-object-ado-md.md) используется аргумент **ActiveConnection** метода [Open,](open-method-ado-md.md) свойство **ActiveConnection** наследует значение аргумента.

Если свойству **ActiveConnection** объекта [catalog](catalog-object-ado-md.md) задайте свойство **Nothing,** связанные данные, включая данные в коллекции [CubeDefs](cubedefs-collection-ado-md.md) и любые связанные объекты [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member.](member-object-ado-md.md) Закрытие объекта **Connection,** который использовался для открытия каталога, имеет тот же эффект, что и установка  **свойству ActiveConnection** свойства **Nothing.**

Изменение базы данных по умолчанию подключения, на которое ссылается свойство **ActiveConnection** объекта **Catalog,** аннулирует содержимое **каталога.**

При попытке изменить свойство **ActiveConnection** для открытого объекта **Cellset** произойдет ошибка.

> [!NOTE]
> В Visual Basic не забудьте использовать ключевое слово **Set** при настройке свойства **ActiveConnection** для объекта **Connection.** Если опустить ключевое слово **Set,** фактически будет установлено свойство **ActiveConnection,** равное свойству по умолчанию объекта **Connection,** **ConnectionString.** Код будет работать; однако вы создадим дополнительное подключение к источнику данных, что может отрицательно сказаться на производительности.

При использовании поставщика данных MSOLAP установите для источника данных в строке подключения имя сервера и уканите в исходном каталоге имя каталога из источника данных. Чтобы подключиться к файлу куба, отключенного от сервера, укажете полный путь к этому файлу. ФАЙЛ СДВ. В любом случае установите для поставщика имя поставщика. Например, следующая строка подключается к каталогу с именем Bobs Video Store на сервере с именем Servername с поставщиком MSOLAP:

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

Следующая строка подключается к локальному файлу куба в расположении C: \\ MSDASDK \\ samples \\ oledb \\ olap \\ data \\ bobsvid.cube:

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

