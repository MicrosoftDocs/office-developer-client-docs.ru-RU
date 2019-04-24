---
title: Отправка команд базовому поставщику данных
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291090"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Отправка команд базовому поставщику данных

**Область применения**: Access 2013, Office 2013

Любая команда, не начинающаяся с фигуры, передается поставщику данных. Это эквивалентно выдаче команды фигуры в форме "SHAPE {Provider Command}". Этим командам *не* требуется создавать **набор записей**. Например, "SHAPE {DROP TABLE MyTable}" — это вполне действительная команда Shape, предполагая, что поставщик данных поддерживает DROP TABLE.

Эта возможность позволяет обычным поставщикам команд и командам форм совместно использовать одно и то же подключение и транзакцию.

