---
title: Действия макроса RestoreWindow
TOCTitle: RestoreWindow Macro Action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2e250bb94f77dd8cfc31c667e9562861b549c23c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875638"
---
# <a name="restorewindow-macro-action"></a>Действия макроса RestoreWindow


**Применимо к**: Access 2013, Office 2013

Действие **RestoreWindow** можно использовать для восстановления предыдущих размеров развернутого или свернутого окна.


> [!NOTE]
> <P>Это действие не может применяться к windows кода в редакторе Visual Basic. Для получения сведений о действиях с кодом windows приведены в разделе свойство <STRONG>WindowState</STRONG> .</P>



## <a name="setting"></a>Параметр

Действие **RestoreWindow** не требует аргументов.

## <a name="remarks"></a>Замечания

Это действие работает на выбранный объект. При свернутых объекта можно выбрать ее с помощью **ВыделитьОбъект** и последующее восстановление предыдущих размеров с помощью действия **RestoreWindow** .

Чтобы переместить или изменить ее размер окна, после восстановления можно использовать действие **MoveAndSizeWindow** .

Действие **RestoreWindow** имеет тот же эффект, как нажать кнопку " **Восстановление** " в правом верхнем углу окна или выбрав команду **восстановить** в **элемент управления** меню.

Чтобы выполнить действие **RestoreWindow** в Visual Basic для приложений (VBA) модуль, используйте метод **восстановления** **объекта** .

