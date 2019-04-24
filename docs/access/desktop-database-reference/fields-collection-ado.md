---
title: Коллекция Fields (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292575"
---
# <a name="fields-collection-ado"></a>Коллекция Fields (ADO)


**Область применения**: Access 2013, Office 2013

Содержит все объекты [field](field-object-ado.md) объекта [Recordset](recordset-object-ado.md) или [записи](record-object-ado.md) .

## <a name="remarks"></a>Замечания

Объект **Recordset** содержит коллекцию **Fields** , состоящего из объектов **field** . Каждый объект **field** соответствует столбцу в наборе **записей**. Вы можете заполнить коллекцию **Fields** перед открытием **набора записей** , вызвав метод [Refresh](refresh-method-ado.md) в коллекции.

> [!NOTE]
> В разделе объект **field** описывается более подробное описание использования объектов **полей** .

Коллекция **Fields** содержит метод [append](append-method-ado.md) , который подготавливает создание и добавление объекта **field** в коллекцию, и метод **Update** , который завершает все добавления и удаления.

Объект **Record** содержит два специальных поля, которые можно индексировать с помощью констант [фиелденум](fieldenum.md) . Одна константа получает доступ к полю, содержащему поток по умолчанию для **записи**, а другой обращается к полю, содержащему строку с АБСОЛЮТНЫМ URL-адресом для **записи**.

Некоторые поставщики (например, [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md)) могут заполнить коллекцию Fields **** подмножеством доступных полей для **записи** или **набора записей**. Другие поля не добавляются в коллекцию до тех пор, пока они не будут первыми ссылаться на них по имени или индексировать код.

При попытке ссылки на несуществующее поле по имени новый объект **field** будет добавлен в коллекцию **Fields** со [статусом](status-property-ado-field.md) **адфиелдпендингинсерт**. Когда вы вызываете [Update](update-method-ado.md), ADO создаст новое поле в источнике данных, если это разрешено поставщиком.

