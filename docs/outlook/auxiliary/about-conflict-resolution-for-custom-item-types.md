---
title: О разрешения конфликтов для типов пользовательских элементов
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: В этом разделе описывается, как разрешать конфликты для типов пользовательских элементов, созданных в Outlook.
ms.openlocfilehash: d85c2022d909901c71c20214f91b316cce81c596
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807665"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>О разрешения конфликтов для типов пользовательских элементов

В этом разделе описывается, как разрешать конфликты для типов пользовательских элементов, созданных в Outlook.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Разрешения конфликтов для стандартных типов элементов Outlook

В Outlook конфликты возникают, когда два или более копий тому же элементу были изменены независимо друг от друга. Outlook обнаруживает конфликты во время синхронизации. Например может обновить элемента собрания через Интернет в Outlook Web App и обновите тому же элементу собрания в Outlook при работе в автономном режиме. Когда Outlook в оперативный режим еще раз и синхронизации данных между компьютером клиента и сервера, оно обнаруживает, что существует два различных копий одного элемента собрания.
  
Когда Outlook синхронизирован элементов, относящихся к стандартный тип элемента Outlook, он учитывает свойств, относящихся к этому типу элемента для выявления возможных конфликтов. Outlook пытается разрешения конфликтов и сохраняет результирующее копию в соответствующую папку без запроса вмешательства пользователя. В тех случаях, когда Outlook считает, что есть вероятность, что результирующее копии не может содержать все необходимые данные Outlook хранит конфликтующие копии в папке "конфликты" в разделе ошибки синхронизации папки. 
  
> [!NOTE]
> Ошибки синхронизации и вложенные в нее папки скрыты до щелкните **Список папок** в области навигации. 
  
В таких случаях пользователям возможность перехода к папке конфликтов для проверки элементов, которые были в конфликт и следует ли использовать копии в папке конфликтов для замены копии, который принял решение Outlook для сохранения.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Разрешения конфликтов для типов пользовательских элементов

### <a name="item-types-and-message-classes"></a>Типы элементов и классов сообщений
  
Все элементы в Outlook связаны с классом сообщения. Например по умолчанию почтового элемента связан с классом сообщения **IPM. Примечание**. Класс сообщения в первую очередь используется для идентификации формы, который должен использоваться для отображения элемента в Outlook. Outlook поддерживает список классов сообщений, которые сопоставляются с типами элементов, встроенный в Outlook. Дополнительные сведения о классах сообщений см. в статье [Item Types and Message Classes](http://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Пользователи могут Создание типов пользовательских элементов, назначить настраиваемые классы сообщения типов пользовательских элементов и использовать настраиваемую форму для отображения типов пользовательских элементов в Outlook. Например вы можете Outlook для отображения сведений о контакте настраиваемых business для бизнес-контактами. Для этого можно создать пользовательский класс сообщения **IPM. Contact.Business**, создайте настраиваемую форму для этого класса сообщений и назначение бизнес-контакты с этим классом сообщения. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Регистрация схема разрешения конфликтов для типов пользовательских элементов
  
При создании типа настраиваемого элемента, отличные от пользовательский класс сообщения и настраиваемых форм необходимо учитывать, как Outlook для обработки конфликтов между копии элемента этого типа элемента. По умолчанию Outlook использует схема разрешения, общие для всех элементов, необходимо учитывать свойств, относящихся к типу элемента и предоставляет конфликтующие копий пользователя для принятия решения. Это так, как типы настраиваемых элементов может определить настраиваемые поля в пользовательскую форму и может иметь настраиваемые свойства и пользовательского кода. Если требуется для рекомендуется свойств конкретного элемента и для разрешения конфликтов с минимальным участием пользователя в Outlook, необходимо указать через параметр реестра Windows. Это можно сделать одним из двух способов: 
  
- С помощью параметра групповой политики на локальном компьютере, который задается в разделе реестра ConflictMsgCls. В следующем примере определяется версии «14.0» для Outlook 2010: 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- Путем прямого изменения раздел реестра пользователя ConflictMsgCls. В следующем примере определяется версии «14.0» для Outlook 2010: 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
Установка разрешения конфликтов посредством групповой политики приоритет над прямого изменения раздела реестра пользователя. Расположение раздела реестра зависит от используемой версии Outlook. Укажите имя класса настраиваемого сообщения как значение в этом разделе. Укажите тип значения в качестве **типа DWORD**и данных значение как одно из значений, представленных в следующей таблице, в зависимости от выбранной схемой решение. 
  
|Данные  | Описание  |
|:-----|:-----|
|0  <br/> |Решение распространенных элемента, которому требуется решение пользователя, как в Outlook 2002 и более ранних версий.  <br/> |
|1  <br/> |Решение распространенных элемента, который требует минимальной пользовательского интерфейса, как используется в Outlook, начиная с Outlook 2003.  <br/> |
|2  <br/> |Решение для почтовых элементов.  <br/> |
|3  <br/> |Определенное разрешение для элементов встреч.  <br/> |
|4  <br/> |Решение для элементов встречи.  <br/> |
|5  <br/> |Определенное разрешение в элементы контактов.  <br/> |
|6  <br/> |Разрешение определенных элементов задачи.  <br/> |
|7  <br/> |Решение об элементах записки.  <br/> |
|8  <br/> |Разрешение определенных элементов журнала.  <br/> |
   
Если указать один из схемы решение конкретного элемента (ключа данных 2-8), Outlook будет пытаться разрешать конфликты в определенных элементов поля (например, **Start** и **End** элемента встречи) автоматически без вмешательства пользователя . Если Outlook считает, что решение может привести к потере важных данных, Outlook будет сохранять конфликтующие копии в папке конфликтов и пользователи могут выбрать для перехода к папке конфликтов заново разрешить эти элементы и переопределить автоматическое вручную решение. 
  
С помощью же деловые контакты приведенном выше примере, если вы хотите указать схема контактов конкретного элемента разрешения для пользовательский класс сообщения **IPM. Contact.Business**, можно добавить его как значение **DWORD** в разделе `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls`и укажите 5 как данные. 
  
> [!NOTE]
> Outlook всегда использует схему решение, характерные для элементов встречи для пользовательских классов сообщений, которые основаны на класс сообщения о встрече, **IPM. Встреча** (например, **IPM. Appointment.Personal**). 
  
## <a name="see-also"></a>См. также

- [Outlook Item Objects](http://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)
