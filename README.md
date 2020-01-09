   def get_field_qs(field, **kwargs):
        if field.name in ['combatant_1', 'combatant_2']:
            return forms.ModelChoiceField(queryset=Tournament.objects.get(id=pk).combatant_pool)
        return field.formfield(**kwargs)