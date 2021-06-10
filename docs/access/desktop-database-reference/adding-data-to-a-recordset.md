---
title: Добавление данных в объект Recordset
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d16eb5871bfe55af58a89cc06b413e8404df8cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280218"
---
# <a name="adding-data-to-a-recordset"></a>Добавление данных в объект Recordset

**Область применения**: Access 2013, Office 2013

**Recordset,** вероятно, является наиболее используемым из объектов ADO. В ADO **recordset** лучше всего подумать как сочетание результата, задаваемого источником данных, и связанных с ним поведения курсоров. Таким образом, можно поместить данные в **набор Recordset,** а затем использовать методы и свойства **Recordset** для навигации по строкам данных, просмотра значений в строках и иного манипулирования набором результатов.

В этом разделе основное внимание будет уделяться добавлению данных в **Набор записей.** Сведения о навигации по данным или обновлении данных см. в главе [4. Редактирование](chapter-4-editing-data.md) данных и глава [5: обновление и обновление данных.](chapter-5-updating-and-persisting-data.md) Для добавления набора результатов в набор  Recordset не всегда требуются расширенные возможности объекта **Command.** Часто можно выполнить команду, задав свойство **Source** в **наборе Recordset** или передав строку команды объекту **Recordset** **Open.**

Существует множество способов добавления данных из источника данных в **набор Recordset.** Используемая методика зависит от потребностей приложения и возможностей поставщика.

