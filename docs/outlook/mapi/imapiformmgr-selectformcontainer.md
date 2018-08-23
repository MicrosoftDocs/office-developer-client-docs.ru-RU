---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f66d0fb1fc9d252ff8b6985c4a54de79313266d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577928"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно, которое позволяет пользователю выбрать контейнер, формы и возвращает интерфейс для объекта контейнера выбранный пользователем.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Дескриптор родительского окна, отображаемого диалогового окна. 
    
 _ulFlags_
  
> [in] Битовая маска флагов, который определяет, как Выбор библиотеки форм (то есть, как контейнер формы установлен). Можно задать следующие флажки:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> Выбор могут поступать из всех контейнеров. Это тип выделения по умолчанию. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> Выбор могут быть созданы только из папки контейнеров.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> Выбор могут быть созданы только из контейнеров, которые не связаны с папками.
    
 _lppfcnt_
  
> [out] Указатель на указатель на возвращенный интерфейс. Этот интерфейс — объект-контейнер, выбранный пользователем.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Средства просмотра формы обычно вызовите метод **IMAPIFormMgr::SelectFormContainer** для выбора формы контейнер, в котором установлен формы. **SelectFormContainer** не может использоваться для выбора контейнера локального формы, который имеет значение HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |Mfcmapi (en) использует метод **IMAPIFormMgr::SelectFormContainer** для выбора контейнера формы перед отображением его содержимого.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

