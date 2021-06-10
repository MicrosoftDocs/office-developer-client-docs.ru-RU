---
title: Коллекция полей (ADO)
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
# <a name="fields-collection-ado"></a>Коллекция полей (ADO)


**Область применения**: Access 2013, Office 2013

Содержит все [объекты Поля](field-object-ado.md) объекта [Recordset](recordset-object-ado.md) или [Record.](record-object-ado.md)

## <a name="remarks"></a>Примечания

Объект **Recordset** имеет коллекцию **Полей,** которая состоит из **объектов Field.** Каждый объект **Field** соответствует столбцу в **Наборе записей.** Вы можете заполнить коллекцию **Полей** перед открытием **Набор записей,** позвонив [методу Обновления](refresh-method-ado.md) в коллекции.

> [!NOTE]
> Дополнительные сведения об использовании объектов **Field** см. в разделе **Объект Field.**

В **коллекции Fields** есть метод [Приложения,](append-method-ado.md) который предварительно создает и добавляет объект **Field** в коллекцию, а также метод **Update,** который завершает любые добавления или удаления.

Объект **Record** имеет два специальных поля, которые можно индексировать с помощью [констант FieldEnum.](fieldenum.md) Один постоянный доступ к поле, содержащее поток записи по **умолчанию,** а другой доступ к поле, содержащее абсолютную строку URL-адреса для **записи**.

Некоторые поставщики (например, поставщик [microsoft OLE DB](microsoft-ole-db-provider-for-internet-publishing.md)для интернет-публикации) могут заполнить коллекцию **Fields** подмножество доступных полей для **Записи** или **Recordset.** Другие поля не будут добавлены в коллекцию, пока они не будут впервые ссылаться по имени или индексироваться кодом.

Если вы попытается ссылаться на несущестующие поля по имени, новый объект [](status-property-ado-field.md) **Field** будет пристроен к коллекции **Fields** со статусом **adFieldPendingInsert.** При [вызове Update](update-method-ado.md)ADO создаст новое поле в источнике данных, если это разрешено поставщиком.

