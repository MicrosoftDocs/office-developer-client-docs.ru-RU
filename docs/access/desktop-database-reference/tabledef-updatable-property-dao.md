---
title: Свойство TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314415"
---
# <a name="tabledefupdatable-property-dao"></a>Свойство TableDef.Updatable (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает на то, можно ли изменить DAO объект. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражения* . Updatable

*выражение*: переменная, представляющая объект **TableDef**.

## <a name="remarks"></a>Комментарии

Параметр **Updatable** свойства всегда true **для** вновь созданного объекта **TableDef** и **False** для связанного **объекта TableDef.** Новый объект **TableDef** может быть придан только базе данных, для которой у текущего пользователя есть разрешение на написание.

