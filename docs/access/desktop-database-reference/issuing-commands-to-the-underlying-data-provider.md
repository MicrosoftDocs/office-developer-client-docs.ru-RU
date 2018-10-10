---
title: Issuing Commands to the Underlying Data Provider
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083f339860e0b28b43e2ceefeaf2cdd1de4b660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480850"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Issuing Commands to the Underlying Data Provider


**Применимо к**: Access 2013 | Office 2013

Любые команды, не начинается с ФИГУРЫ передается через поставщика данных. Это эквивалентно команды фигуры в форме «ФИГУРЫ {поставщика команды}». Выполните эти команды *не* имеет для создания **записей**. Для экземпляра «ФИГУРЫ {РАЗМЕЩЕНИЯ ТАБЛИЦУ MyTable} — это команда действителен фигуры, при условии, что поставщик данных поддерживает размещения сообщений в ТАБЛИЦЕ.

Эта возможность позволяет как обычный поставщика команды и фигуры для совместного использования одного подключения и транзакций.

