---
title: Свойство DefaultDatabase (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 01ca42ff738afe3a35cab6263cdae32ac256f3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294150"
---
# <a name="defaultdatabase-property-ado"></a>Свойство DefaultDatabase (ADO)


**Область применения**: Access 2013, Office 2013

Указывает базу данных по умолчанию для объекта [Connection.](connection-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строку,** которая оценивается в качестве имени базы данных, доступной у поставщика.

## <a name="remarks"></a>Заметки

Используйте свойство **DefaultDatabase** для настройки или возврата имени базы данных по умолчанию для определенного объекта **Connection.**

Если имеется база данных по умолчанию, SQL строки могут использовать неквалифицированный синтаксис для доступа к объектам в этой базе данных. Чтобы получить доступ к объектам в базе данных, не указанной в свойстве **DefaultDatabase,** необходимо квалифицировать имена объектов с нужным именем базы данных. После подключения поставщик записи данных базы данных по умолчанию в **свойство DefaultDatabase.** Некоторые поставщики позволяют использовать только одну базу данных на подключение, в этом случае изменить свойство **DefaultDatabase** невозможно.

Некоторые источники данных и поставщики могут не поддерживать эту функцию и возвращать ошибку или пустую строку.

**Использование удаленной службы данных** Это свойство не доступно для объекта подключения на **стороне** клиента.

