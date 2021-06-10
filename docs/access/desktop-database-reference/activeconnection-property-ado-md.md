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

Указывает, к каков объектУ ADO [Connection](connection-object-ado.md) текущий ячейки или каталог в настоящее время принадлежит.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает **вариант,** содержащий строку, определяющий объект подключения или **подключения.** По умолчанию пусто.

## <a name="remarks"></a>Примечания

Это свойство можно настроить на допустимый объект ADO **Connection** или допустимую строку подключения. Когда это свойство заданной строке подключения, поставщик создает новый объект **Подключения** с помощью этого определения и открывает подключение.

Если для открытия объекта [Cellset](cellset-object-ado-md.md) используется аргумент **ActiveConnection** метода [Open,](open-method-ado-md.md) свойство **ActiveConnection** наследует значение аргумента.

Настройка свойства **ActiveConnection** объекта [Каталога](catalog-object-ado-md.md) в **Nothing** освобождает связанные данные, в том числе данные из коллекции [CubeDefs](cubedefs-collection-ado-md.md) и любые связанные объекты [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member.](member-object-ado-md.md) Закрытие **объекта Подключения,** который использовался для открытия **каталога,** имеет тот же эффект, что и установка свойства **ActiveConnection** в **Nothing.**

Изменение базы данных по умолчанию подключения, ссылающегося на свойство **ActiveConnection** объекта **Каталог,** аннулирует содержимое **каталога.**

Ошибка будет возникать при попытке изменить свойство **ActiveConnection** на открытый объект **Cellset.**

> [!NOTE]
> В Visual Basic не забудьте использовать ключевое слово **Set** при настройке свойства **ActiveConnection** для **объекта Подключения.** Если вы не закроете ключевое слово **Set,** вы фактически  задасте свойство **ActiveConnection,** равное свойству объекта Подключения по **умолчанию, ConnectionString.** Код будет работать; однако будет создаваться дополнительное подключение к источнику данных, что может иметь негативные последствия для производительности.

При использовании поставщика данных MSOLAP установите источник данных в строке подключения к имени сервера и установите начальный каталог имени каталога из источника данных. Чтобы подключиться к файлу куба, отсоединяемом от сервера, установите расположение на полный путь к . ФАЙЛ CUB. В любом случае установите поставщику имя поставщика. Например, следующая строка подключается к каталогу с именем Bobs Video Store на сервере с именем Servername с поставщиком MSOLAP:

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

Следующая строка подключается к локальному файлу куба в расположении C: \\ MSDASDK примеры \\ \\ oledb olap данных \\ \\ \\ bobsvid.cub:

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

