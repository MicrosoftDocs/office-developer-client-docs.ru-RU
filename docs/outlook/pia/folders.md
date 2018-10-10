---
title: Папки
TOCTitle: Folders
ms:assetid: b72b5705-d77a-4cad-873d-457b9fb6553e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184634(v=office.15)
ms:contentKeyID: 55119856
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: e0fd6aa6ff6a7c4d6c4821858aa8d2a3ca60b2c3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406430"
---
# <a name="folders"></a>Папки

В этом разделе приведены примеры задач, в которых используются папки. Объекты [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) представляют иерархию папок, в которой хранятся элементы Microsoft Outlook. К таким папкам относятся папки календаря, почты и удаленных элементов. В основной сборке взаимодействия Outlook (PIA) элементы объекта **Folder** предоставляются в виде элементов объекта [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)).

## <a name="in-this-section"></a>В этой статье

|Раздел|Описание|
|:----|:----------|
|[Добавление папки в список папок](how-to-add-a-folder-to-the-folder-list.md) |Использование метода [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) для добавления папки в список папок Outlook.|
|[Перечисление папок](how-to-enumerate-folders.md)  |Перечисление папок путем итерации по коллекциям папок.|
|[Получение папки по умолчанию и перечисление вложенных в нее папок](how-to-get-a-default-folder-and-enumerate-its-subfolders.md) |Получение папки по умолчанию в хранилище по умолчанию пользователя и перечисление вложенных в нее папок.|
|[Получение папки на основе пути к ней](how-to-get-a-folder-based-on-its-folder-path.md)  |Использование пути к папке и получение связанной папки.|
|[Выбор папки и отображение сведений о папке](how-to-select-a-folder-and-display-folder-information.md)  |Отображение программным способом сведений о папке, выбранной пользователем из определенного списка папок.|
|[Получение класса сообщений по умолчанию для папки](how-to-get-the-default-message-class-of-a-folder.md)  |Использование свойства [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) для получения класса сообщений по умолчанию для папки.|
|[Доступ к данным решений, хранящимся в скрытом сообщении в папке](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)  |Использование объекта [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) для извлечения данных, которые хранятся в виде скрытого сообщения определенного класса сообщений в папке.|
|[Проверка поддержки настраиваемых свойств элемента в запросах на уровне папки](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md) |Проверка того, что при добавлении настраиваемого свойства к типу элемента в папку также добавляется свойство, обеспечивающее запрос настраиваемого свойства на уровне папки.|

## <a name="see-also"></a>См. также

- [Календарь](calendar.md)
- [Контакты](contacts.md)
- [Почта](mail.md)
- [Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

