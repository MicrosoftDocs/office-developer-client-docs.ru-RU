---
title: Подготовленное свойство (ADO)
TOCTitle: Prepared property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9541b2d584728c09ee852f628cdfc35f3d170f04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301458"
---
# <a name="prepared-property-ado"></a>Подготовленное свойство (ADO)


**Область применения**: Access 2013, Office 2013

Указывает, следует ли сохранять скомпилировали версию команды перед выполнением.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Boolean,** которое, если задано **значение True,** указывает, что команда должна быть подготовлена.

## <a name="remarks"></a>Примечания

Используйте свойство **Prepared,** чтобы поставщик сохранить подготовленную (или компилировать) версию запроса, [](command-object-ado.md) указанного в свойстве [CommandText](commandtext-property-ado.md) перед первым выполнением объекта Command. Это может замедлить первое выполнение команды, но после компиляции команды поставщик будет использовать компиляторную версию команды для любых последующих выполнения, что приведет к повышению производительности.

Если свойство **false,** поставщик будет выполнять объект **Command** напрямую, не создавая компиляторную версию.

Если поставщик не поддерживает подготовку команд, он может возвращать ошибку, как только это свойство заданной **для True.** Если ошибка не возвращается, она просто игнорирует запрос на подготовку команды и задает свойство **Prepared** **false**.

