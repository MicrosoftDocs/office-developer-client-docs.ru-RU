---
title: Update Resync Property--Dynamic (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16600f22084718a6b32656ebfc56d6a9be06c676
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481332"
---
# <a name="update-resync-property--dynamic-ado"></a>Update Resync Property--Dynamic (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает, будет ли метод [UpdateBatch](updatebatch-method-ado.md) следуют неявных [выполнить повторную синхронизацию](resync-method-ado.md) метод операцию и если да, области действия этой операции.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает один или несколько [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) значения.

## <a name="remarks"></a>Замечания

Значения ADCPROP\_UPDATERESYNC\_ENUM может быть объединен, за исключением adResyncAll, который уже представляет сочетание остальные значения.

Константы **adResyncConflicts** хранятся значения повторной синхронизации как базового значения, но не переопределяет ожидающих изменений.

**Обновление выполнить повторную синхронизацию** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта [набора записей](recordset-object-ado.md) при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.

