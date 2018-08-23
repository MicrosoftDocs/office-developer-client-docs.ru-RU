---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3c6242c9a926341908cb86645a8ea8586a9ca598
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586356"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Предоставляет диалоговое окно, которое позволяет пользователю выбрать форму и возвращает объект данные формы с описанием данной форме.
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Дескриптор родительского окна, отображаемого диалогового окна. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип строк, переданное. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _pszTitle_
  
> [in] Указатель на строку, которая содержит заголовок диалогового окна. Если параметр _pszTitle_ имеет значение NULL, поставщик библиотеки форм предоставляет заголовок по умолчанию. 
    
 _pfld_
  
> [in] Указатель на папку для выбора формы. Если параметр _pfld_ имеет значение NULL, форма можно выбирать из контейнера формы local, личный или организации. 
    
 _ppfrminfoReturned_
  
> [out] Указатель на указатель на объект сведения возвращенные формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Средства просмотра формы вызвать метод **IMAPIFormMgr::SelectForm** для первым диалоговое окно, которое позволяет пользователю выбрать формы и затем для получения объекта данные формы, описывающий выбранной формы. Диалоговое окно ограничения, предписывающие пользователю выбрать одну форму. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Диалоговое окно **SelectForm** отображает только формы, которые не являются скрытыми (то есть, форм, имеющих их скрытые свойства снимите флажок). Если форма просмотра передает флаг MAPI_UNICODE в параметре _ulFlags_ , все строки содержат Юникод. Поставщики библиотеки форм, которые не поддерживают строк в кодировке Юникод должен возвращать MAPI_E_BAD_CHARWIDTH, если передается MAPI_UNICODE. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |Mfcmapi (en) использует метод **IMAPIFormMgr::SelectForm** для выбора формы и отправки информации о формы для одного или нескольких журналов.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

