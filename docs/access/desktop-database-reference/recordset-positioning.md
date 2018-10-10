---
title: Recordset Positioning
TOCTitle: Recordset Positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10586c711b9931c1cac93401111f4d477ca8a987
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482884"
---
# <a name="recordset-positioning"></a>Recordset Positioning


**Применимо к**: Access 2013 | Office 2013

Используйте свойство **AbsolutePosition** для перемещения к записи на основании его порядковый номер в объекте **набора записей** или для определения порядковый номер текущей записи. Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.

**AbsolutePosition** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**. Как уже было сказано ранее, можно получить общее число записей в объекте **набора записей** из свойства **RecordCount** .

Если задать свойство **AbsolutePosition** даже в том случае, если это записи в текущей кэш-памяти, ADO перезагружает кэша с новой группы записей, начиная с указанной записи. Свойство **CacheSize** определяет размер этой группы.


> [!NOTE]
> <P>Не следует использовать свойство <STRONG>AbsolutePosition</STRONG> как номер заменяющего записи. Положение данной записи изменений при удалении предыдущей записи. Кроме того, не Software assurance, что данной записи будут иметь же <STRONG>AbsolutePosition</STRONG> , если опросить или повторном открытии в объект <STRONG>набора записей</STRONG> . Закладки являются рекомендуемый способ сохранения и возврата в заданной позиции и являются единственным способом размещения для всех типов объектов <STRONG>наборов записей</STRONG> .</P>


