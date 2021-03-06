---
title: ��������� ����� MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e1287a3-0f15-4d9a-b7ee-738fce9cd51f
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: b22b8641d55037d3755fc9ae32b97455223bbd12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431941"
---
# <a name="mapi-receive-folders"></a>��������� ����� MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
����� ��������� �������� �������� ��������� ������ ������������� ���������. ��������� �����, ����� ���������� ����� � ���������, ��������� �������� ��������� ��� MAPI. MAPI ����� ��� ��������� ����� �� ���������: �������� ����� ��������� ��������� � ����� "��������" ��������� ����������� ����� � ��� ��������� (IPM). � �������� ����� � ��������� ��������� � ��� �������� �� ��������� �������� ����� ��� ���� ��������� ����� ���������� ��������������.
  
 �������� ����� "��������" � MAPI ��� ������� ������ ��������� ��������� � ��������� ��� �������� �� ��������� �������� ����� ��� ��������� ������� ���������: 
  
- ����� ��������� IPM.
    
- ����� ��������� ������.
    
- ������ ��� �����������, �����.
    
��� ��������� �������, ������� ��, ������� ������������ � ����� �� ��������� ���������������� ��������, ���������� � ����� "��������". ���������������� �������� ���������� ����������, ������� ������������ ����������� ������ ����� ������� ���������� �������� ����� ��������� ��� ������������� ������ ������. ��������, ���� ������ ���������� ��� ��������� ��������� � ������� ������ ���������������� ��������. Paper.Order, �� ������ ������� ����� [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) , ����� ���������� ����� ��������� ������� � ������� ������ Report.IPC.Paper.Order. 
  
��������� �����, ������ �������� �� ������������� ����������� ������� ���������. ������� ����� ���� ���������� ����� ����� ��������� ����� � ����� ��������� ��� ����� ��������� MAPI �� ���������. ��� ������� ������� ��������� ���� �����, ����� �������� ��������� ��� �������� ������ � ���� ��� ����������. �������� �������� ������ ����� ���������� ����� ��� ��������� � ������� ������ **MyClass**. ��� ��������� ��������� � ������ **MyClass.Home** ��� **MyClass.Home.Kitchen.Computer**������� ��� ��������� ����� ��������� � ����� ��������� ��� �������� ������ **MyClass**.
  
���������� ��� ��������� ������, ������� ������� ����� ������������ ��� ������ � �������� ����� ���������.
  
- [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)
    
- [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)
    
- [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)
    
� ������� ����� ��������� �������� ������ ��������� �������� ��� ���� ����� ���������, ������������� ��� �������� ���������. ��� ����� ������������ ������� �������� ����� ���������, ���� ������ � ������������� ������.
  
To retrieve a receive folder for a particular message class, clients pass the message class string to the [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) method. The message store provider returns an entry identifier for the corresponding folder. To implement **GetReceiveFolder**, a message store provider should use an algorithm that selects the folder whose associated message class matches the longest possible prefix of the specified message class. For example, assume the message store has the following associations between receive folders and message classes in its receive folder table:
  
- **IPM** ��������� ���������� � ����� "��������". 
    
- **IPM.Note.Sample** ��������� ���������� � ����� ��������. 
    
� ��������� ������� ��������, ��� ��������� � ��������� ������ ����� ���������� ��������������� �������� �����.
  
|**����� �������� ���������**|**��������� �����**|
|:-----|:-----|
|**IPM. Note.Sample.Simple** <br/> |������� �����  <br/> |
|**IPM.Note** <br/> |����� "��������"  <br/> |
|**IPM. Карта времени** <br/> |����� "��������"  <br/> |
|**IPM. Note.Sample.Simple.Totally** <br/> |������� �����  <br/> |
   
������� �������� ����� **SetReceiveFolder** ����� ������ ����� ����� ������������� ��������� � �������� �����. ����� ��������� ������������ � ����� ������ ���������, MAPI �������� ��� � ����� ���������, ������������ ��� �������� ������ ������. � ������� ���� ������ ����� ����� ��������� ����������� ��� ��������� � ������� ������ **IPM** � �������� ��������� � ������� ������ **IPM.Note.Test**, ��� ��������� ����� ������� � ����� ��������� ��� ������ ��������� **IPM**. 
  
� ����� **SetReceiveFolder**������� ������ ��������� ������ ����� ��������� � �������� ������������� ������ ����� �����. ��� �� ����� ������� ����� �������� �������� NULL ��� ������ ��� ����� ���� ����������. � ��������� ������� ����������� ���������, ���������� �� �������� NULL ���������� ������������� ������ � ������ ���������. 
  
|**��������  _SetReceiveFolder_**|**�������� ���������**|
|:-----|:-----|
|������������� ������ ������ �������� NULL  <br/> |��������� ��������� ������� ����� ����� ���������� ���������, ����� � ��� ������������� �������� �����. ����� �������� ����� �� ���������. <br/> ����������� ������ **GetReceiveFolder** � ���� ������� ��������� ���������� ����� ��������� ��� �������� ������ ���������; ��� ����� �������� ��������� **GetReceiveFolder** ���������� ����� ��������� � ��������� IPM.  <br/> |
|����� ���������, ������� �������� NULL  <br/> |��������� ��������� ��������� ����� ��� ������ ������ ��������� � ��������� �����. �����, � ��������� ������ �������������� �������� ��������� ����� ��������� � ��� �����.  <br/> |
|������������� ������ � ����� ��������� ������ �������� NULL  <br/> |��������� ��������� ������� ����� �����/����� ��� ������ ������ ���������. �� ������� ������������� ��� ��������� �������� NULL, ��� ��� ��� ������ �������� �������� ��������� � �������� ����� ��������� ��������� � �����, ������� �������� ��������� ��� �������.  <br/> |
   
���� ����� ��������� ������� �� ������ ���� ������, ����� ����������� ����� ������ ���������. ��������� ��������� ��������������� �� ���������� ����� ��������� **IPM** ��� ����� ��������� ���������, ��� ������� ������ �����; ���������� ���������� ����������� ���������� **IPM.Note** ��� ����� ��� ��������� ���������, ��� ������� ����� ������ �����. 
  
## <a name="see-also"></a>См. также



[����� MAPI](mapi-folders.md)

