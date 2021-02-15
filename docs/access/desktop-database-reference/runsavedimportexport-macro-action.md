---
title: Макрокоманда RunSavedImportExport
TOCTitle: RunSavedImportExport macro action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: adcc8a2a9462509f4b37d2dbdaf824387ae52a26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309177"
---
# <a name="runsavedimportexport-macro-action"></a>Макрокоманда RunSavedImportExport

**Область применения**: Access 2013, Office 2013

Действие **RunSavedImportExport** можно использовать для запуска сохраненной спецификации импорта или экспорта, созданной с помощью мастера импорта или мастера экспорта.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных.

## <a name="setting"></a>Параметр

Действие **RunSavedImportExport** имеет следующий аргумент.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Сохраненное имя экспорта импорта</strong></p></td>
<td><p>В выпадаемом списке выберите имя сохраненной спецификации импорта или экспорта.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

- Это макрос действует так же, как и выполнение следующей процедуры в Access:
    
  1.  На **вкладке "Внешние данные"** щелкните **"Сохраненные импорты"** или **"Сохраненные экспорты".**
    
  2.  В **диалоговом** окне "Управление задачами  данных" на вкладке "Сохраненные импорты" или "Сохраненные экспорты" (в зависимости от вашего выбора на предыдущем шаге) щелкните спецификацию, которую нужно запустить. 
    
  3.  Нажмите кнопку **Выполнить**.

- Перед запуском действия **RunSavedImportExport** убедитесь, что файлы источника и назначения существуют, исходные данные готовы к импорту и что операция не перезапишет данные в файле назначения случайно.

- Ссылки на дополнительные сведения о сохранении и запуске спецификаций импорта и экспорта см. в разделе **"См. также".**

- Если сохраненная спецификация импорта или экспорта, выбираемая для аргумента **saved Import Export Name,** удаляется после создания макроса, Access отображает следующее сообщение об ошибке при запуске макроса: спецификация с указанным индексом не **существует. Укажите другой индекс. '******specification name****'.**

