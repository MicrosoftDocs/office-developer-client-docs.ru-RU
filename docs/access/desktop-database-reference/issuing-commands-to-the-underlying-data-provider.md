---
title: Выполнения команд базового поставщика данных
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 142772aaff5080a6e2522ab31884f2ff2319c8a7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944636"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Выполнения команд базового поставщика данных

**Применимо к**: Access 2013, Office 2013

Любые команды, не начинается с ФИГУРЫ передается через поставщика данных. Это эквивалентно команды фигуры в форме «ФИГУРЫ {поставщика команды}». Выполните эти команды *не* имеет для создания **записей**. Для экземпляра «ФИГУРЫ {РАЗМЕЩЕНИЯ ТАБЛИЦУ MyTable} — это команда действителен фигуры, при условии, что поставщик данных поддерживает размещения сообщений в ТАБЛИЦЕ.

Эта возможность позволяет как обычный поставщика команды и фигуры для совместного использования одного подключения и транзакций.

